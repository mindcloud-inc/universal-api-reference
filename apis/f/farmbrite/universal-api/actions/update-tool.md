# Farmbrite: Update tool

Updates an existing tool in Farmbrite.

```
PUT https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/update-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/update-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "toolId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/update-tool', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "toolId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `toolId` | string | yes |  |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "brand": "string",
      "contactId": "string",
      "costPerUnit": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": "string",
      "datePurchased": "string",
      "description": "string",
      "electronicId": "string",
      "engine": "string",
      "estimatedValue": "string",
      "id": "string",
      "insured": true,
      "latitude": "string",
      "longitude": "string",
      "manualUrl": "https://example.com",
      "modelNumber": "string",
      "name": "Ava Chen",
      "plateNumber": "string",
      "purchased": true,
      "serialNumber": "string",
      "status": "string",
      "transmission": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usageAlertEmail": "ava@example.com",
      "usageAlertInterval": "string",
      "usageAlertSent": "string",
      "usageLevel": "string",
      "usageUnit": "string",
      "year": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `brand` | string |  |
| `contactId` | string |  |
| `costPerUnit` | string |  |
| `createdAt` | date |  |
| `customFields` | string |  |
| `datePurchased` | string |  |
| `description` | string |  |
| `electronicId` | string |  |
| `engine` | string |  |
| `estimatedValue` | string |  |
| `id` | string |  |
| `insured` | boolean |  |
| `latitude` | string |  |
| `longitude` | string |  |
| `manualUrl` | string |  |
| `modelNumber` | string |  |
| `name` | string |  |
| `plateNumber` | string |  |
| `purchased` | boolean |  |
| `serialNumber` | string |  |
| `status` | string |  |
| `transmission` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `usageAlertEmail` | string |  |
| `usageAlertInterval` | string |  |
| `usageAlertSent` | string |  |
| `usageLevel` | string |  |
| `usageUnit` | string |  |
| `year` | string |  |

## Native endpoint

Through the native Farmbrite API, this operation is `PUT /tools/:tool_id` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tool.md) for the provider-specific parameters and requirements.

