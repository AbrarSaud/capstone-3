# Real Estate Auction Platform 🏘️💼

## 📌 Project Overview

This is a **Real Estate Intermediary Platform**.  
It allows **property owners** to list their properties and lets **customers** join **online auctions** by location.  
The platform makes buying and selling properties **faster**, **easier**, and **more organized**.

---

## 🚀 Main Features

-  **Property Management** – Add, update, and delete property listings  
-  **Auction Management** – Create and control auctions  
-  **Real-Time Bidding** – Customers can place bids live during auctions  
-  **Auto-Expiry** – Auctions end automatically when the time is finished  

---

## 🛠️ Technologies & Tools

| Tool / Technology         | Purpose                          |
|---------------------------|----------------------------------|
| `Spring Boot`             | Backend development framework    |
| `Spring Data JPA`         | Work with the database           |
| `Spring Web`              | Build RESTful APIs               |
| `Spring Validation`       | Validate user input              |
| `Spring Mail`             | Send email notifications         |
| `MySQL`                   | Store and manage data            |
| `Lombok`                  | Reduce boilerplate code          |
| `OpenPDF`                 | Generate PDF reports             |
| `Postman`                 | Test the API endpoints           |
| `Maven`                   | Dependency and build manager     |

---

## 📂 API Endpoints

### Admin Endpoints

| # | Entity | Endpoint | Description |
|---|--------|----------|-------------|
| 1 | Admin | `GET /unapproved-properties` | Get list of properties not approved yet |
| 2 | Admin | `GET /admin/active-auctions-without-bids` | Show all active auctions with no bids |
| 3 | Admin | `PUT /disable-owner/{ownerId}` | Blacklist (disable) an owner by ID |
| 4 | Admin | `PUT /end-auction-early/{auctionId}` | Admin ends auction early for any reason |
| 5 | Admin | `GET /admin/auction-stats` | Get auction stats (ended/active) |
| 6 | Admin | `POST /owners/send-welcome-emails` | Send welcome email to all owners |
| 7 | Admin | `PUT /enable-owner/{{ownerId}}` | Remove from Blacklist owner by ID  |

### Owner Endpoints

| # | Entity | Endpoint | Description |
|---|--------|----------|-------------|
| 8 | Owner | `GET /owners/{ownerId}/active-auctions` | Show all active auctions for owner's properties |
| 9 | Owner | `PUT /{ownerId}/property-title-update/{propertyId}` | Update title of unapproved property |

### Customer Endpoints

| # | Entity | Endpoint | Description |
|---|--------|----------|-------------|
| 10 | Customer | `PUT /customers/{id}/withdraw-bid/{bidId}` | Withdraw a bid by customer |
