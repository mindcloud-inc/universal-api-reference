# <img src="https://images.mindcloud.co/apps/icons/zippopotamus_1777583764500.png" alt="Zippopotamus logo" width="28" height="28"> Zippopotamus: Universal API

Look up postal codes, places, and nearby locations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zippopotamus/latest
- **Category:** Business Intelligence / Data Warehouse
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zippopotam.us
- **Vendor API docs:** https://docs.zippopotam.us/docs/v1/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Nearby Places by Postal Code](actions/list-nearby-places-by-postal-code.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zippopotamus/latest/actions/list-nearby-places-by-postal-code?connectionId=$CONNECTION_ID&country=US&postalcode=90210" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Location

| Action | Method | Description |
| --- | --- | --- |
| [List Nearby Places by Postal Code](actions/list-nearby-places-by-postal-code.md) | GET | Retrieves nearby places in Zippopotamus by postal code. |
| [List Postal Codes by Place](actions/list-postal-codes-by-place.md) | GET | Retrieves postal codes in Zippopotamus by place name. |
| [Look Up Places by Postal Code](actions/lookup-places-by-postal-code.md) | GET | Retrieves places in Zippopotamus by postal code. |

