# Vectorizer AI: Download



```
GET https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/download
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectorizer AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/download?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/download?${params}`, {
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
| `output.file_format` | list | no | One of: `dxf`, `eps`, `pdf`, `png`, `svg`. Default: `svg`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `receipt` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vectorizer AI API returns.

## Native endpoint

Through the native Vectorizer AI API, this operation is `POST /download` (base URL `https://api.vectorizer.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download.md) for the provider-specific parameters and requirements.

