# CloudContactAI: Requeue Campaign



```
PUT https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/requeue-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/requeue-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/requeue-campaign', {
  method: 'PUT',
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
| `campaignId` | string | no | The campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": 1,
      "id": 1,
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
| `clientId` | number |  |
| `id` | number |  |
| `message` | string |  |
| `stats` | object |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `POST api/v2/campaigns/:campaignId/requeue` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/requeue-campaign.md) for the provider-specific parameters and requirements.

