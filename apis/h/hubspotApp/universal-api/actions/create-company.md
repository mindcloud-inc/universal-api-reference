# HubSpot: Create Company

Creates a new company in HubSpot.

```
POST https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `associations[].to` | object | no |  |
| `associations[].to.id` | string | no | Id of the object to associate |
| `associations[].types[].associationCategory` | list | no | This represents if the association you're creating is default created by HupSpot, or it is a custom association the user defined. |
| `properties` | object | no |  |
| `properties.name` | string | no |  |
| `associations[]` | array<object> | no |  |
| `associations[].types[]` | array<object> | no |  |
| `associations[].types[].associationTypeId` | string | no | Check for types at: https://developers.hubspot.com/docs/api-reference/crm-associations-v4/guide#association-type-id-values |
| `properties.domain` | string | no |  |
| `properties.city` | string | no |  |
| `properties.industry` | string | no |  |
| `properties.phone` | string | no |  |
| `properties.state` | string | no |  |
| `properties.lifecycleStage` | string | no |  |
| `properties.address` | string | no |  |
| `properties.acumatica_customer_id` | string | no |  |
| `properties.acumatica_location_id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "string",
      "id": "string",
      "properties": {
        "createdate": "string",
        "domain": {},
        "hsLastmodifieddate": "string",
        "hsObjectId": "string",
        "name": "Ava Chen"
      },
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | string |  |
| `id` | string |  |
| `properties.createdate` | string |  |
| `properties.domain` | object |  |
| `properties.hsLastmodifieddate` | string |  |
| `properties.hsObjectId` | string |  |
| `properties.name` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/companies` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

