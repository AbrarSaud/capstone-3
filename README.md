## API Endpoints

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
