# APImage: Enhance Prompt

Rewrites a prompt for AI image generation in APImage.

```
POST https://connect.mindcloud.co/v1/universal/aPImage/latest/actions/enhance-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a APImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aPImage/latest/actions/enhance-prompt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "a dog on a beach"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aPImage/latest/actions/enhance-prompt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "a dog on a beach"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | Prompt to rewrite into a more descriptive image-generation prompt. Example: `a dog on a beach`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native APImage API returns.

## Native endpoint

Through the native APImage API, this operation is `POST https://app.apimage.org/api/v1/image-studio` (base URL `https://apimage.org/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enhance-prompt.md) for the provider-specific parameters and requirements.

