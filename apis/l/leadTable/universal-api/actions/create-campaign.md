# LeadTable: Create campaign



```
POST https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerID": "string",
  "occupation": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerID": "string",
    "occupation": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerID` | string | yes | The customer that will own the campaign. |
| `occupation` | string | yes | Campaign or table name. |
| `funnelLink` | string | no | Optional funnel link for the campaign. |
| `preQualify` | boolean | no | Whether leads should be pre-qualified. |
| `deleteLeads` | boolean | no | Whether existing leads should be deleted. |
| `tableAndProfileConfig[]` | array<object> | no | Optional configuration array for table and profile fields. |
| `overrideValues` | object | no | Optional object of override values. |
| `status[]` | array<string> | no | Optional list of statuses for the campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerID": "string",
      "customerName": "Ava Chen",
      "id": "string",
      "occupation": "string",
      "webhookToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `customerID` | string |  |
| `customerName` | string |  |
| `id` | string |  |
| `occupation` | string |  |
| `webhookToken` | string |  |

## Native endpoint

Through the native LeadTable API, this operation is `POST /table/create` (base URL `https://api.lead-table.com/api/v3/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

