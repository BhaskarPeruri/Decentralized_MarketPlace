# Decentralized Market Place

This Solidity smart contract represents a basic marketplace where users can list items, place orders, and complete transactions. 

# Here's a brief explanation of the key components:


**Struct Item:**

    Represents an item that can be listed in the marketplace.

    Contains fields for the item's name, description, price, seller's address, and availability status.

**Mapping items:**

    Associates each item ID with its corresponding Item struct.

    Allo ws checking of item details by their IDs.

**State variable itemCount:**

    Keeps track of the total number of items listed in the marketplace.

**Events:**

    ItemListed: Triggered when a new item is listed in the marketplace.
    
    OrderPlaced: Triggered when a buyer places an order for a specific item.
    
    TransactionCompleted: Triggered when a transaction is successfully completed.

**Constructor:**

    Initializes the itemCount to 0 when the contract is deployed.

# **Functions:**

**1.listItem:**

    Allows sellers to list a new item in the marketplace.
    
    Increments itemCount to generate a unique item ID.
    
    Emits the ItemListed event.

**2.Function placeOrder:**

    Allows buyers to place an order for a specific item.
    
    Checks for valid item ID, availability, and correct payment amount.
    
    Marks the item as unavailable.
    
    Emits the OrderPlaced event.

**3.Function completeTransaction:**


    Allows buyers to complete a transaction for a specific item.
    
    Checks for valid item ID, unavailable status, and ensures that the sender is not the seller.
    
    Transfers the payment to the seller.
    
    Emits the TransactionCompleted event.

**4.Function getItem:**


    Allows users to retrieve information about a specific item by providing its ID.
    
    Checks for valid item ID and returns the details of the item.

**Modifiers and Requirements:**

The contract uses various require statements to enforce conditions such as valid item ID, item availability, correct payment amount, and preventing sellers from placing orders or completing transactions.

Please note that this is a basic example, and in a real-world scenario, additional features, security measures, and optimizations would be necessary.
