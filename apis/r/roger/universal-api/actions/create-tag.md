# Roger: Create Tag



```
POST https://connect.mindcloud.co/v1/universal/roger/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Roger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/roger/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/roger/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Tag title. |
| `backgroundColor` | string | no | Optional tag background color hex code. |
| `textColor` | string | no | Optional tag text color hex code. |
| `description` | string | no | Optional tag description. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Roger API returns.

## Native endpoint

Through the native Roger API, this operation is `POST /tags` (base URL `https://api.rogerroger.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

