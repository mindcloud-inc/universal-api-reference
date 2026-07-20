# HubSpot: Create Deal

Creates a new deal in HubSpot.

```
POST https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-deal', {
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
| `properties` | object | no | The deal properties payload. |
| `properties.dealname` | string | no | The deal name. |
| `properties.dealstage` | string | no | The deal stage value. |
| `properties.pipeline` | string | no | The pipeline value. |
| `associations[]` | array<object> | no | Associations to create with the deal. |
| `associations[].to` | object | no | The association target. |
| `associations[].to.id` | string | no | The associated record ID. |
| `associations[].types[]` | array<object> | no | The association type definitions. |
| `associations[].types[].associationCategory` | string | no | The HubSpot association category. |
| `associations[].types[].associationTypeId` | number | no | The HubSpot association type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the deal is archived. |
| `createdAt` | date | When the deal was created. |
| `id` | string | The created deal record ID. |
| `properties` | object | The returned deal properties. |
| `updatedAt` | date | When the deal was last updated. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/deals` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

