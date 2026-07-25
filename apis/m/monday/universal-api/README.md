# <img src="https://images.mindcloud.co/apps/icons/monday-com-default_1782232945550.png" alt="Monday logo" width="28" height="28"> Monday: Universal API

Monday through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/monday/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Boards](actions/get-boards.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monday/latest/actions/get-boards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST |  |
| [Create Sub Item](actions/create-sub-item.md) | POST | Creates a new subitem in Monday. |
| [Create Update Record](actions/create-update-record.md) | POST |  |
| [Delete Update Record](actions/delete-update-record.md) | DELETE |  |
| [Get All SubItems Of Of an Item by Item's Column Value](actions/get-all-sub-items-of-of-an-item-by-items-column-value.md) | POST | Retrieves items and their subitems from a Monday board by column value. |
| [Get Board By Id](actions/get-board-by-id.md) | GET |  |
| [Get Board Items](actions/get-board-items.md) | POST |  |
| [Get Board Items by Column Value](actions/get-board-items-by-column-value.md) | POST |  |
| [Get Board Items with Sub Items](actions/get-board-items-sub-items.md) | POST | Retrieves board items and subitems from a Monday board. |
| [Get Boards](actions/get-boards.md) | GET |  |
| [Get Boards With items](actions/get-boards-with-items.md) | GET | Retrieves items and their subitems from a Monday board by column value. |
| [Get Boards With items (GraphQL)](actions/get-boards-with-items-graph-ql.md) | GET |  |
| [Get Columns](actions/get-columns.md) | POST |  |
| [Get Item Details](actions/get-item-details.md) | POST |  |
| [Get Item Details with Connect Board Item ID's](actions/get-item-details-with-connect-board-item-i-ds.md) | POST | Retrieves item details and linked board items from Monday. |
| [Search In Board With Item Name](actions/search-in-board-with-item-name.md) | POST | Finds a board item in Monday by name. |
| [Send Notifications](actions/send-notifications.md) | POST | Sends a notification to a user in Monday. |
| [Update Multiple Column Values](actions/update-multiple-column-values.md) | POST |  |
| [Update Payment Status](actions/update-payment-status.md) | POST |  |
| [Update Payment Status Sub-Item](actions/update-payment-status-sub-item.md) | POST |  |

