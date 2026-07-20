# <img src="https://images.mindcloud.co/apps/icons/unnamed-12_1774876626218.png" alt="Handwrite logo" width="28" height="28"> Handwrite: Universal API

Handwrite lets you automate handwritten letters by listing available handwriting and stationery options, sending letters, and checking order status through the Handwrite REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/handwrite/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.handwrite.io/
- **Vendor API docs:** https://documentation.handwrite.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Handwritings](actions/list-handwritings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/list-handwritings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Handwriting

| Action | Method | Description |
| --- | --- | --- |
| [List Handwritings](actions/list-handwritings.md) | GET | Retrieves handwritings from Handwrite. |

### Letter

| Action | Method | Description |
| --- | --- | --- |
| [Send Letter](actions/send-letter.md) | POST | Sends a handwritten letter through Handwrite. |

### Letter Batch

| Action | Method | Description |
| --- | --- | --- |
| [Send Batch Letters](actions/send-batch-letters.md) | POST | Sends batch letters through Handwrite. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Handwrite. |

### Stationery

| Action | Method | Description |
| --- | --- | --- |
| [List Stationery](actions/list-stationery.md) | GET | Retrieves stationery from Handwrite. |

