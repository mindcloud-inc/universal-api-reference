# Kylas CRM: Create Lead

Creates a new lead in Kylas CRM.

```
POST https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kylas CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/create-lead', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "aging": 1,
      "createdAt": "string",
      "createdBy": 1,
      "createdViaId": "string",
      "createdViaName": "Ava Chen",
      "createdViaType": "string",
      "id": 1,
      "lastName": "Chen",
      "metaData": {},
      "ownerId": 1,
      "recordActions": {},
      "score": 1,
      "updatedAt": "string",
      "updatedBy": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aging` | number | Lead aging value reported by Kylas. |
| `createdAt` | string | UTC timestamp when the lead was created. |
| `createdBy` | number | User ID that created the lead. |
| `createdViaId` | string | Identifier for the source that created the lead. |
| `createdViaName` | string | Display name of the source that created the lead. |
| `createdViaType` | string | Type of the source that created the lead. |
| `id` | number | Kylas lead ID. |
| `lastName` | string | Lead last name. |
| `metaData` | object | Additional Kylas metadata for related display names. |
| `ownerId` | number | Owner user ID for the lead. |
| `recordActions` | object | Action permissions available on this lead record. |
| `score` | number | Kylas lead score. |
| `updatedAt` | string | UTC timestamp when the lead was last updated. |
| `updatedBy` | number | User ID that last updated the lead. |

## Native endpoint

Through the native Kylas CRM API, this operation is `POST /leads` (base URL `https://api.kylas.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

