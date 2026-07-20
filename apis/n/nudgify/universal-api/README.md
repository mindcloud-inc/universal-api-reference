# <img src="https://images.mindcloud.co/apps/icons/images_1773975746500.png" alt="Nudgify logo" width="28" height="28"> Nudgify: Universal API

Send sign-ups and purchases to power social proof nudges

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nudgify/latest
- **Category:** Marketing
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nudgify.com
- **Vendor API docs:** https://www.nudgify.com/docs/categories/for-developers/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Create Conversion](actions/create-conversion.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nudgify/latest/actions/create-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversions[]": [
    {}
  ],
  "conversions[].date": "string"
}'
```

## Actions (2)

### Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversion](actions/create-conversion.md) | POST | Creates conversion events in Nudgify. |

### Purchase

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase](actions/create-purchase.md) | POST | Creates purchase events in Nudgify. |

