# CometAPI: Runway Generate

Creates a Runway text-to-video task in CometAPI.

```
POST https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/runway-generate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/runway-generate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/runway-generate', {
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
      "status": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `task_id` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `POST /runway/pro/generate` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/runway-generate.md) for the provider-specific parameters and requirements.

