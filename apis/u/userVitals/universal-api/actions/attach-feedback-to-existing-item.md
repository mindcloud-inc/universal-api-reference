# UserVitals: Attach Feedback To Existing Item

Attaches feedback to an existing idea or story.

```
PUT https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/attach-feedback-to-existing-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/attach-feedback-to-existing-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parentId": "string",
  "parentToken": "string",
  "sourceId": "string",
  "sourceToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/attach-feedback-to-existing-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parentId": "string",
    "parentToken": "string",
    "sourceId": "string",
    "sourceToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parentId` | string | yes | The target idea or story id. |
| `parentToken` | string | yes | The target idea or story token. |
| `sourceId` | string | yes | The feedback id to attach. |
| `sourceToken` | string | yes | The feedback token to attach. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UserVitals API returns.

## Native endpoint

Through the native UserVitals API, this operation is `POST /feedback/attach` (base URL `https://app.roadmap.space/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attach-feedback-to-existing-item.md) for the provider-specific parameters and requirements.

