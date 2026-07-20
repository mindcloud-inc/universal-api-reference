# Mendato: Create Estimate



```
POST https://connect.mindcloud.co/v1/universal/mendato/latest/actions/create-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/create-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendato/latest/actions/create-estimate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | yes | GraphQL variables object for the Mendato create estimate mutation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createEstimate": {
        "estimate": {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "estimateDate": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "number": 1,
          "numberPrefix": "string",
          "status": "string",
          "validityDate": "2026-05-07T12:00:00.000Z",
          "webEnabled": true,
          "webUrl": "https://example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createEstimate.estimate.createdAt` | date |  |
| `createEstimate.estimate.estimateDate` | date |  |
| `createEstimate.estimate.id` | string |  |
| `createEstimate.estimate.number` | number |  |
| `createEstimate.estimate.numberPrefix` | string |  |
| `createEstimate.estimate.status` | string |  |
| `createEstimate.estimate.validityDate` | date |  |
| `createEstimate.estimate.webEnabled` | boolean |  |
| `createEstimate.estimate.webUrl` | string |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-estimate.md) for the provider-specific parameters and requirements.

