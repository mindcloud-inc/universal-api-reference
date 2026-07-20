# VdoCipher: Update Video Parameters

Updates video parameters in VdoCipher.

```
PUT https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/update-video-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/update-video-parameters" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/update-video-parameters', {
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
| `keys` | string | no | CSV value of keys |
| `values` | string | no |  |
| `videoId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native VdoCipher API returns.

## Native endpoint

Through the native VdoCipher API, this operation is `POST /videos/:videoId/params` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-video-parameters.md) for the provider-specific parameters and requirements.

