# <img src="https://images.mindcloud.co/apps/icons/moonto-checkpad-icon_1776434042778.png" alt="MOONTO Shopping Lists - Checkpad logo" width="28" height="28"> MOONTO Shopping Lists - Checkpad: Universal API

Access MOONTO shopping lists, checkpads, list items, and related events through the official MOONTO API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mOONTOShoppingListsCheckpad/latest
- **Category:** Commerce
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.moonto.app/products/checkpad
- **Vendor API docs:** https://api.moonto.app/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/list-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Checkpad

| Action | Method | Description |
| --- | --- | --- |
| [Get Checkpad Details](actions/get-checkpad-details.md) | GET | Retrieves current checkpad details from Checkpad. |
| [List Checkpads](actions/list-checkpads.md) | GET | Retrieves a list of checkpads from Checkpad. |

### Checkpad Event

| Action | Method | Description |
| --- | --- | --- |
| [List Checkpad Events](actions/list-checkpad-events.md) | GET | Retrieves checkpad event records from Checkpad. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Get List Details](actions/get-list-details.md) | GET | Retrieves shopping list details from Checkpad. |
| [List Lists](actions/list-lists.md) | GET | Retrieves a list of shopping lists from Checkpad. |

### List Event

| Action | Method | Description |
| --- | --- | --- |
| [List List Events](actions/list-list-events.md) | GET | Retrieves shopping list events from Checkpad. |

### List Item

| Action | Method | Description |
| --- | --- | --- |
| [Add List Item](actions/add-list-item.md) | POST | Creates a new shopping list item in Checkpad. |
| [Check List Item](actions/check-list-item.md) | PUT | Marks a shopping list item as done in Checkpad. |
| [Delete List Item](actions/delete-list-item.md) | DELETE | Deletes a shopping list item from Checkpad. |
| [List List Items](actions/list-list-items.md) | GET | Retrieves shopping list items from Checkpad. |

