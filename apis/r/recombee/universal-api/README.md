# <img src="https://images.mindcloud.co/apps/icons/recombee_1776265462140.png" alt="Recombee logo" width="28" height="28"> Recombee: Universal API

Recombee integration with HMAC-signed API key auth and database-scoped REST endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/recombee/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.recombee.com
- **Vendor API docs:** https://docs.recombee.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Items](actions/list-items.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recombee/latest/actions/list-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Batch Result

| Action | Method | Description |
| --- | --- | --- |
| [Batch](actions/batch.md) | POST | Creates a batch request in Recombee. |

### Bookmark Event

| Action | Method | Description |
| --- | --- | --- |
| [Add Bookmark](actions/add-bookmark.md) | POST | Creates a bookmark event in Recombee. |

### Bulk Item Update Result

| Action | Method | Description |
| --- | --- | --- |
| [Update More Items](actions/update-more-items.md) | PUT | Updates multiple items in your Recombee catalog. |

### Cart Addition Event

| Action | Method | Description |
| --- | --- | --- |
| [Add Cart Addition](actions/add-cart-addition.md) | POST | Creates a cart addition event in Recombee. |

### Detail View Event

| Action | Method | Description |
| --- | --- | --- |
| [Add Detail View](actions/add-detail-view.md) | POST | Creates a detail view event in Recombee. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Add Item](actions/add-item.md) | POST | Creates a new item in Recombee. |
| [Get Item Values](actions/get-item-values.md) | GET | Retrieves values for an item from Recombee. |
| [List Items](actions/list-items.md) | GET | Retrieves items from your Recombee catalog. |
| [Set Item Values](actions/set-item-values.md) | PUT | Updates values for an item in Recombee. |

### Item Property

| Action | Method | Description |
| --- | --- | --- |
| [Add Item Property](actions/add-item-property.md) | POST | Creates a new item property in Recombee. |
| [Get Item Property Info](actions/get-item-property-info.md) | GET | Retrieves details for an item property in Recombee. |
| [List Item Properties](actions/list-item-properties.md) | GET | Retrieves item properties from your Recombee database. |

### Purchase Event

| Action | Method | Description |
| --- | --- | --- |
| [Add Purchase](actions/add-purchase.md) | POST | Creates a purchase event in Recombee. |

### Rating Event

| Action | Method | Description |
| --- | --- | --- |
| [Add Rating](actions/add-rating.md) | POST | Creates a rating event in Recombee. |

### Recommendation

| Action | Method | Description |
| --- | --- | --- |
| [Recommend Items to Item](actions/recommend-items-to-item.md) | GET | Retrieves item recommendations for an item from Recombee. |
| [Recommend Items to User](actions/recommend-items-to-user.md) | GET | Retrieves item recommendations for a user from Recombee. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Items](actions/search-items.md) | GET | Searches items for a user in Recombee. |

### Series

| Action | Method | Description |
| --- | --- | --- |
| [Add Series](actions/add-series.md) | POST | Creates a new series in Recombee. |
| [Insert to Series](actions/insert-to-series.md) | POST | Adds items to a series in Recombee. |
| [List Series](actions/list-series.md) | GET | Retrieves series from your Recombee database. |

### Series Item

| Action | Method | Description |
| --- | --- | --- |
| [List Series Items](actions/list-series-items.md) | GET | Retrieves items from a Recombee series. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Add User](actions/add-user.md) | POST | Creates a new user in Recombee. |
| [Get User Values](actions/get-user-values.md) | GET | Retrieves values for a user from Recombee. |
| [List Users](actions/list-users.md) | GET | Retrieves users from your Recombee database. |
| [Set User Values](actions/set-user-values.md) | PUT | Updates values for a user in Recombee. |

### User Merge Result

| Action | Method | Description |
| --- | --- | --- |
| [Merge Users](actions/merge-users.md) | PUT | Merges one user into another in Recombee. |

### User Property

| Action | Method | Description |
| --- | --- | --- |
| [Add User Property](actions/add-user-property.md) | POST | Creates a new user property in Recombee. |
| [Get User Property Info](actions/get-user-property-info.md) | GET | Retrieves details for a user property in Recombee. |
| [List User Properties](actions/list-user-properties.md) | GET | Retrieves user properties from your Recombee database. |

### View Portion Event

| Action | Method | Description |
| --- | --- | --- |
| [Set View Portion](actions/set-view-portion.md) | POST | Creates a view portion event in Recombee. |

