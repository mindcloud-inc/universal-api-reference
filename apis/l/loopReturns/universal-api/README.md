# <img src="https://images.mindcloud.co/apps/icons/favicon-32x32_1755106158710.png" alt="Loop Returns logo" width="28" height="28"> Loop Returns: Universal API

Loop Returns through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/loopReturns/latest
- **Category:** Commerce
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.loopreturns.com
- **Vendor API docs:** https://docs.loopreturns.com/api-reference/authentication

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Returns](actions/list-returns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/list-returns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Flag Return

| Action | Method | Description |
| --- | --- | --- |
| [Flag Return](actions/flag-return.md) | POST | Flag a return in Loop for review. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Destinations](actions/list-destinations.md) | GET | Retrieve all destinations. |

### Process Return

| Action | Method | Description |
| --- | --- | --- |
| [Process Return](actions/process-return.md) | PUT | Process a return in Loop based on the return ID. Processing a return will archive it in Loop and fulfill any remaining outcomes, such as… |

### Returns

| Action | Method | Description |
| --- | --- | --- |
| [Get Return Details](actions/list-return-details.md) | GET | Get the details of a specific return based on a return’s ID, an order name, or a Shopify order ID. |
| [List Returns](actions/list-returns.md) | GET | Pull a detailed list of returns created within a given timeframe. |

