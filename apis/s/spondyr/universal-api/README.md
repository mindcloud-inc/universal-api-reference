# <img src="https://images.mindcloud.co/apps/icons/spondyr-square-icon_1775157487478.png" alt="Spondyr logo" width="28" height="28"> Spondyr: Universal API

Spondyr is a correspondence platform for generating, delivering, tracking, and administering templates and related configuration through its REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/spondyr/latest
- **Category:** Communication / Email Communications
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.spondyr.io/
- **Vendor API docs:** https://client.spondyr.io/Public/Public/APIDocumentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Transaction Types](actions/list-transaction-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/list-transaction-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Condition](actions/create-condition.md) | POST | Creates a new condition for a transaction type in Spondyr. |
| [Create Transaction Type](actions/create-transaction-type.md) | POST | Creates a new transaction type in Spondyr. |
| [Delete Condition](actions/delete-condition.md) | DELETE | Deletes an existing condition for a transaction type from Spondyr. |
| [Delete Transaction Type](actions/delete-transaction-type.md) | DELETE | Deletes an existing transaction type from Spondyr. |
| [Get Condition](actions/get-condition.md) | GET | Retrieves a condition for a transaction type in Spondyr. |
| [Get Transaction Type](actions/get-transaction-type.md) | GET | Retrieves a transaction type from Spondyr. |
| [List Conditions](actions/list-conditions.md) | GET | Retrieves conditions for a transaction type in Spondyr. |
| [List Transaction Types](actions/list-transaction-types.md) | GET | Retrieves transaction types from Spondyr. |
| [Update Condition](actions/update-condition.md) | PUT | Updates an existing condition for a transaction type in Spondyr. |
| [Update Transaction Type](actions/update-transaction-type.md) | PUT | Updates an existing transaction type in Spondyr. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Type](actions/create-event-type.md) | POST | Creates a new event type for a transaction type in Spondyr. |
| [Delete Event Type](actions/delete-event-type.md) | DELETE | Deletes an existing event type for a transaction type from Spondyr. |
| [Get Event Type](actions/get-event-type.md) | GET | Retrieves an event type for a transaction type in Spondyr. |
| [List Event Types](actions/list-event-types.md) | GET | Retrieves event types for a transaction type in Spondyr. |
| [Update Event Type](actions/update-event-type.md) | PUT | Updates an existing event type for a transaction type in Spondyr. |

