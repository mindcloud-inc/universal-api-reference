# HelpDocs: Update Clip

Updates an existing clip in HelpDocs.

```
PUT https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/update-clip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDocs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/update-clip" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clipId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/update-clip', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clipId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clipId` | string | yes | Clip ID to update. |
| `content` | string | no | Updated clip content. |
| `title` | string | no | Updated clip title. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HelpDocs API returns.

## Native endpoint

Through the native HelpDocs API, this operation is `PATCH /clip/:clip_id` (base URL `https://api.helpdocs.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-clip.md) for the provider-specific parameters and requirements.

