```mermaid
sequenceDiagram
    participant Client
    participant Server
    
    Note over Client, Server: 1. Initialization
    Client->>Server: GET / (Home Page)
    Server-->>Client: 200 OK + Set-Cookie (JSESSIONID)
    
    Note over Client, Server: 2. Authentication
    Client->>Server: POST /login (username/password + Cookie)
    Server-->>Client: 302 Found (Redirect to Dashboard)
    
    Note over Client, Server: 3. Discovery
    Client->>Server: GET /categories (Request category list)
    Server-->>Client: 200 OK + Returns ProductID list
    
    Note over Client, Server: 4. Selection
    Client->>Server: GET /product-view (ItemID)
    Server-->>Client: 200 OK + Item Details
    
    Note over Client, Server: 5. Transaction
    Client->>Server: POST /add-to-cart (ItemID + Quantity + Cookie)
    Server-->>Client: 200 OK (Cart Updated)
