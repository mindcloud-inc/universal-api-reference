# <img src="https://images.mindcloud.co/apps/icons/split-csv_1774455571544.png" alt="Split CSV logo" width="28" height="28"> Split CSV: Universal API

Split and transform delimited text files

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/splitCSV/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.splitcsv.com
- **Vendor API docs:** https://www.splitcsv.com/developers/core/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Profile](actions/retrieve-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/retrieve-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new file-processing order in Split CSV. |
| [Get Order Status](actions/get-order-status.md) | GET | Retrieves the status of an order in Split CSV. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Profile](actions/retrieve-profile.md) | GET | Retrieves the current user profile from Split CSV. |

