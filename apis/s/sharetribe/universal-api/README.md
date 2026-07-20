# <img src="https://images.mindcloud.co/apps/icons/sharetribe_1773688999969.png" alt="Sharetribe logo" width="28" height="28"> Sharetribe: Universal API

Sharetribe: Manage marketplace users, listings, and transactions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sharetribe/latest
- **Category:** Commerce
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sharetribe.com/
- **Vendor API docs:** https://www.sharetribe.com/api-reference/integration.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query Users](actions/query-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/query-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Availability Exception

| Action | Method | Description |
| --- | --- | --- |
| [Create Availability Exceptions](actions/create-availability-exceptions.md) | POST | Creates new availability exceptions in Sharetribe. |
| [Delete Availability Exceptions](actions/delete-availability-exceptions.md) | DELETE | Deletes existing availability exceptions from Sharetribe. |
| [Query Availability Exceptions](actions/query-availability-exceptions.md) | GET | Retrieves availability exceptions from Sharetribe. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Query Events](actions/query-events.md) | GET | Retrieves events from Sharetribe. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Upload Image](actions/upload-image.md) | POST | Uploads an image to Sharetribe. |

### Listing

| Action | Method | Description |
| --- | --- | --- |
| [Approve Listing](actions/approve-listing.md) | PUT | Approves an existing listing in Sharetribe. |
| [Close Listing](actions/close-listing.md) | PUT | Closes an existing listing in Sharetribe. |
| [Create Listing](actions/create-listing.md) | POST | Creates a new listing in Sharetribe. |
| [Open Listing](actions/open-listing.md) | PUT | Opens an existing listing in Sharetribe. |
| [Query Listings](actions/query-listings.md) | GET | Retrieves listings from Sharetribe. |
| [Show Listing](actions/show-listing.md) | GET | Retrieves a listing from Sharetribe. |
| [Update Listing](actions/update-listing.md) | PUT | Updates an existing listing in Sharetribe. |

### Stock Adjustment

| Action | Method | Description |
| --- | --- | --- |
| [Create Stock Adjustment](actions/create-stock-adjustment.md) | POST | Creates a new stock adjustment in Sharetribe. |
| [Query Stock Adjustments](actions/query-stock-adjustments.md) | GET | Retrieves stock adjustments from Sharetribe. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Query Transactions](actions/query-transactions.md) | GET | Retrieves transactions from Sharetribe. |
| [Show Transaction](actions/show-transaction.md) | GET | Retrieves a transaction from Sharetribe. |
| [Speculatively Transition Transaction](actions/speculatively-transition-transaction.md) | PUT | Speculatively transitions a transaction in Sharetribe. |
| [Transition Transaction](actions/transition-transaction.md) | PUT | Transitions an existing transaction in Sharetribe. |
| [Update Transaction Metadata](actions/update-transaction-metadata.md) | PUT | Updates existing transaction metadata in Sharetribe. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Approve User](actions/approve-user.md) | PUT | Approves an existing user in Sharetribe. |
| [Query Users](actions/query-users.md) | GET | Retrieves users from Sharetribe. |
| [Show User](actions/show-user.md) | GET | Retrieves a user from Sharetribe. |
| [Update User Profile](actions/update-user-profile.md) | PUT | Updates an existing user profile in Sharetribe. |

