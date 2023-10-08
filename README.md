# Inmentory_Management_system
A simple inventory management sytem written in HTML, CSS and PHP


Entities:

    User
        UserID (Primary Key)
        Username
        Password (hashed and salted for security)
        UserType (Admin or Regular User)

    Item
        ItemID (Primary Key)
        ItemName
        Description
        Quantity
        Price
        UserID (Foreign Key, references User.UserID)

Relationships:

    User (1) ----- (0 or many) Item
    (One user can have zero or many items, indicating they can add multiple items to the inventory)

Functionality:

    Only users with UserType = 'Admin' can delete items.

Here's a visual representation of the ERD:


+----------------+          +-----------------+
|     User       |          |       Item      |
+----------------+          +-----------------+
| UserID (PK)    |          | ItemID (PK)     |
| Username       |          | ItemName        |
| Password       |          | Description      |
| UserType       |          | Quantity         |
+----------------+          | Price            |
                           | UserID (FK)      |
                           +-----------------+
