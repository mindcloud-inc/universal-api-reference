# Moderation API: Submit Content For Moderation

Submits content to Moderation API for moderation.

```
POST https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/submit-content-for-moderation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/submit-content-for-moderation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/submit-content-for-moderation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | object | yes | The content sent for moderation |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timestamp` | number | no | Unix timestamp (in milliseconds) of when the content was created. Use if content is not submitted in real-time. |
| `channel` | string | no | Provide a channel ID or key. Will use the project's default channel if not provided. |
| `contentId` | string | no | The unique ID of the content in your database. |
| `metaType` | string | no | The meta type of content being moderated |
| `authorId` | string | no | The author of the content. |
| `conversationId` | string | no | For example the ID of a chat room or a post |
| `metadata` | object | no | Any metadata you want to store with the content |
| `doNotStore` | boolean | no | Do not store the content. The content won't enter the review queue |
| `policies[]` | array<object> | no | (Enterprise) override the channel policies for this moderation request only. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "content": {},
      "errors": [
        {}
      ],
      "evaluation": {},
      "insights": [
        {}
      ],
      "meta": {},
      "policies": [
        {}
      ],
      "recommendation": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `content` | object | Potentially modified content. |
| `errors` | array<object> | Policies that had errors |
| `evaluation` | object | The evaluation of the content after running the channel policies. |
| `insights` | array<object> | Results of all insights enabled in the channel. |
| `meta` | object | Metadata about the moderation request |
| `policies` | array<object> | Results of all policies in the channel. Sorted by highest probability. |
| `recommendation` | object | The recommendation for the content based on the evaluation. |

## Native endpoint

Through the native Moderation API API, this operation is `POST /moderate` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-content-for-moderation.md) for the provider-specific parameters and requirements.

