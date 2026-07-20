# Discourse: Update Post

Updates an existing post in Discourse.

```
PUT https://connect.mindcloud.co/v1/universal/discourse/latest/actions/update-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/update-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "post.raw": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/update-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "post.raw": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Post id to update. |
| `post.raw` | string | yes | Updated raw post body. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `post.edit_reason` | string | no | Optional edit reason visible in post history. |
| `bypass_bump` | boolean | no | Skip bumping the topic when updating the post. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "post": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `post` | object |  |

## Native endpoint

Through the native Discourse API, this operation is `PUT /posts/:id.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-post.md) for the provider-specific parameters and requirements.

