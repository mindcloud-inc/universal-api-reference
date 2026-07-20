# Sendible: Get Link Preview



```
GET https://connect.mindcloud.co/v1/universal/sendible/latest/actions/get-link-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/get-link-preview?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendible/latest/actions/get-link-preview?${params}`, {
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
| `url` | string | yes | The link to preview. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "caption": "string",
      "description": "string",
      "href": "string",
      "media": [
        {}
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caption` | string |  |
| `description` | string |  |
| `href` | string |  |
| `media` | array<object> |  |
| `name` | string |  |

## Native endpoint

Through the native Sendible API, this operation is `GET api/v0/linkpreview.json` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-preview.md) for the provider-specific parameters and requirements.

