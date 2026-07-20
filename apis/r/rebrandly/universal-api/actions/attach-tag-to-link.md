# Rebrandly: Attach Tag To Link

Attaches a tag to a link in Rebrandly.

```
PUT https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/attach-tag-to-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/attach-tag-to-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lid": "string",
  "tid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/attach-tag-to-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lid": "string",
    "tid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lid` | string | yes | Unique identifier of the link to update. |
| `tid` | string | yes | Unique identifier of the tag to attach. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rebrandly API returns.

## Native endpoint

Through the native Rebrandly API, this operation is `POST /links/:lid/tags/:tid` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attach-tag-to-link.md) for the provider-specific parameters and requirements.

