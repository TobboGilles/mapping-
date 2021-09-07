pragma solidity ^0.8.6;


contract Mapping {
    
mapping (uint => book) public books;
mapping (address => mapping(uint => book)) public Mymapping;
    
    struct book {
        string title; 
        string author;
    }
    
    
    function addbook (uint _id, string memory _title, string memory _author) public {
        books[_id] = book (_title, _author);
        
    } 
    
    function ajouterBook(uint _id, string memory _title, string memory _author)public {
        Mymapping[msg.sender][_id] = book (_title, _author);
    }
    
 }

