# HelpDocs: Create Clip

Creates a new clip in HelpDocs.

```
POST https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/create-clip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDocs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/create-clip" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/create-clip', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Clip title. |
| `content` | string | yes | Clip content. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HelpDocs API returns.

## Native endpoint

Through the native HelpDocs API, this operation is `POST /clip` (base URL `https://api.helpdocs.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-clip.md) for the provider-specific parameters and requirements.

