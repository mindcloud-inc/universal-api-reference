# Papyrs: Post To Page Discussion



```
POST https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/post-to-page-discussion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papyrs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/post-to-page-discussion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "msg": "string",
  "pageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/post-to-page-discussion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "msg": "string",
    "pageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `msg` | string | yes | The message to post to the page discussion. |
| `pageId` | string | yes | The Papyrs page ID. |

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

Through the native Papyrs API, this operation is `POST /feed/post/:page_id/` (base URL `https://{{credentials.subdomain}}.papyrs.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-to-page-discussion.md) for the provider-specific parameters and requirements.

