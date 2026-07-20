# Ayrshare: Generate Auto Hashtags

Adds relevant hashtags to a post in Ayrshare.

```
POST https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/generate-auto-hashtags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/generate-auto-hashtags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "post": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/generate-auto-hashtags', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "post": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `post` | string | yes | Post text to generate relevant hashtags for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "hashtags": [
        "string"
      ],
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Ayrshare error code. |
| `hashtags` | array<string> | Generated hashtags. |
| `message` | string | Generation or error message. |
| `status` | string | Hashtag generation status. |

## Native endpoint

Through the native Ayrshare API, this operation is `POST /hashtags/auto` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-auto-hashtags.md) for the provider-specific parameters and requirements.

