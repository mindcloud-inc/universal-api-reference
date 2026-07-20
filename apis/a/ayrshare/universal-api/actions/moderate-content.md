# Ayrshare: Moderate Content

Checks text for harmful or inappropriate content in Ayrshare.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/moderate-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/moderate-content?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/moderate-content?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | Text to submit for moderation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "results": {},
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
| `message` | string | Moderation or error message. |
| `results` | object | Moderation result details. |
| `status` | string | Moderation status. |

## Native endpoint

Through the native Ayrshare API, this operation is `POST /validate/moderation` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/moderate-content.md) for the provider-specific parameters and requirements.

