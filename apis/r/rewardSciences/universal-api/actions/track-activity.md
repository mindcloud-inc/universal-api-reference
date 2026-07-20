# Reward Sciences: Track Activity



```
POST https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/track-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reward Sciences `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/track-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idp": "string",
  "identity": "string",
  "activityType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/track-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idp": "string",
    "identity": "string",
    "activityType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idp` | string | yes | Identity provider name. |
| `identity` | string | yes | Identity value within the provider. |
| `activityType` | string | yes | Case-insensitive activity identifier. |
| `fields` | object | no | Optional custom metadata object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Tracked activity ID. |
| `user_id` | number | User ID associated with the tracked activity. |

## Native endpoint

Through the native Reward Sciences API, this operation is `POST /activities` (base URL `https://api.rewardsciences.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-activity.md) for the provider-specific parameters and requirements.

