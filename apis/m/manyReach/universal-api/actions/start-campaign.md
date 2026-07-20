# ManyReach: Start Campaign

Starts a campaign in ManyReach.

```
PUT https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/start-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/start-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/start-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the campaign to start. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | number |  |
| `status` | string |  |

## Native endpoint

Through the native ManyReach API, this operation is `POST https://api.manyreach.com/api/v2/campaigns/:id/start` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-campaign.md) for the provider-specific parameters and requirements.

