# Papyrs: Post To Activity Stream



```
POST https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/post-to-activity-stream
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papyrs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/post-to-activity-stream" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "msg": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/post-to-activity-stream', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "msg": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `msg` | string | yes | The message to post to the activity stream. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "a": "string",
      "by": "string",
      "c": "string",
      "id": 1,
      "unsafe_c": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `a` | string | Avatar URL. |
| `by` | string | Display name of the author. |
| `c` | string | Posted message content. |
| `id` | number | Papyrs feed entry ID. |
| `unsafe_c` | string | Unescaped message content. |

## Native endpoint

Through the native Papyrs API, this operation is `POST /feed/post/` (base URL `https://{{credentials.subdomain}}.papyrs.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-to-activity-stream.md) for the provider-specific parameters and requirements.

