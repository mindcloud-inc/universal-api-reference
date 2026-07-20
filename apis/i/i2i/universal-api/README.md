# i2i: Universal API

i2i Fulfillment is a Canadian omnichannel fulfillment and supply-chain partner with Vancouver and Toronto distribution centres. This app exposes read-only ship order lookups for the i2i IBIS API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/i2i/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.i2i.ca/
- **Vendor API docs:** https://www.i2i.ca/why-i2i/our-software

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List ship orders](actions/list-ship-orders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/i2i/latest/actions/list-ship-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Ship Order

| Action | Method | Description |
| --- | --- | --- |
| [Create order](actions/create-order.md) | POST | Creates a new ship order in i2i. |
| [Get ship order](actions/get-ship-order.md) | GET | Retrieves a ship order from i2i by order ID. |
| [List ship orders](actions/list-ship-orders.md) | GET | Retrieves ship orders from i2i by status and date range. |

