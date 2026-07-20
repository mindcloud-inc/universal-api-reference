# Vectorizer AI: Delete



```
DELETE https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/delete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectorizer AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/delete?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/delete?${params}`, {
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
| `image.token` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | True when the image token has been affirmatively deleted. |

## Native endpoint

Through the native Vectorizer AI API, this operation is `POST /delete` (base URL `https://api.vectorizer.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete.md) for the provider-specific parameters and requirements.

