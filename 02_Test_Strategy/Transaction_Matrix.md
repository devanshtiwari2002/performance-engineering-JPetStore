###  JMeter Transaction & Scripting Matrix

This matrix maps out the technical properties, validation priorities, dynamic data requirements, and current development status for each scripted user transaction.

| Transaction ID | Transaction Name | HTTP Method | Priority | Dynamic Data / Correlation | Script Status |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **T01** | Home Page | `GET` | High | No |  Pending |
| **T03** | Login Form | `GET` | Critical | **Yes** *(Session Token)* | Pending |
| **T05** | Account Creation | `POST` | Critical | **Yes** *(Form Payload)* |  Pending |
| **T06** | View Category | `GET` | High | **Yes** *(Category ID)* |  Pending |
| **T07** | View Product | `GET` | High | **Yes** *(Product ID)* |  Pending |
| **T08** | Shopping Cart | `GET` | Critical | **Yes** *(Session State)* |  Pending |
| **T09** | Update Cart (Value) | `POST` | Low | No |  Pending |
| **T10** | Checkout Page | `GET` | High | **Yes** *(Order Context)* |  Pending |
| **T11** | Order Confirm | `POST` | Critical | **Yes** *(Form Parameters)* |  Pending |
| **T12** | Confirmation Details | `GET` | High | **Yes** *(Dynamic Order ID)* |  Pending |
