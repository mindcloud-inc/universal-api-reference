# Ritekit: Get Link Preview

Retrieves a link preview from Ritekit.

```
GET https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-link-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ritekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-link-preview?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-link-preview?${params}`, {
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
| `url` | string | yes | URL to generate a link preview for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "image": "string",
      "message": "string",
      "result": true,
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `image` | string |  |
| `message` | string |  |
| `result` | boolean |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Ritekit API, this operation is `GET /v2/text/link-preview` (base URL `https://api.ritekit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-preview.md) for the provider-specific parameters and requirements.

