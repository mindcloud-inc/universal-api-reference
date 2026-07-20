# CloudContactAI: Create Direct Campaign



```
POST https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/create-direct-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/create-direct-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/create-direct-campaign', {
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
| `clientId` | string | no | The client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {},
      "clientId": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isDefault": true,
      "message": "string",
      "stats": {},
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `clientId` | number |  |
| `createdDate` | date |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `message` | string |  |
| `stats` | object |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `POST api/clients/:clientId/campaigns/direct` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-direct-campaign.md) for the provider-specific parameters and requirements.

