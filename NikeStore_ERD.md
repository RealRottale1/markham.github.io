```mermaid
---
title: Nike Store Data Base
---
erDiagram
    Products {
        String ProductId PK
        String ProductName
        String ProductDescription
        Money Cost
    }
    Products }|--|| Sales : "Is Sold On"
    Products }|--|| Inventory : "Is Tracked On"


    Customers {
        String CustomerId PK
        String Name
        Int Age
        String Sex
        String Payment_Method
    }
    Customers }|--o{ Sales : "Places"

    Sales{
        String ProductId FK
        String CustomerId FK
        Money Cost FK
        DateTime Time_Of_Purchase
        Int Quantity
    }
    Inventory{
        String ProductId FK
        String ProductName FK
        String ProductDescription FK
        Int Amount_In_Stock
        String Location
    }