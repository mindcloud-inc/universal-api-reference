# 1minAI: Generate social media posts

Creates social media posts in 1minAI.

```
POST https://connect.mindcloud.co/v1/universal/minAI/latest/actions/generate-social-media-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1minAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minAI/latest/actions/generate-social-media-posts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "postType": "linkedin",
  "prompt": "Announce a new product launch"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minAI/latest/actions/generate-social-media-posts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "postType": "linkedin",
    "prompt": "Announce a new product launch"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `postType` | list | yes | One of: `Facebook`, `Instagram`, `LinkedIn`, `TikTok`, `X`. Default: `linkedin`. |
| `prompt` | string | yes | Example: `Announce a new product launch`. |
| `tone` | string | no | Default: `Informative`. |
| `language` | string | no | Default: `English`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiRecord": {},
      "temporaryUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiRecord` | object |  |
| `temporaryUrl` | string |  |

## Native endpoint

Through the native 1minAI API, this operation is `POST /api/features` (base URL `https://api.1min.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-social-media-posts.md) for the provider-specific parameters and requirements.

