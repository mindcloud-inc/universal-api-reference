# Mallabe: Get Website Thumbnail

Retrieves a website thumbnail from Mallabe.

```
GET https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/get-website-thumbnail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mallabe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/get-website-thumbnail?connectionId=$CONNECTION_ID&website=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "website": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/get-website-thumbnail?${params}`, {
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
| `website` | string | yes | Website URL to capture. |
| `webhookUrl` | string | no | Webhook URL for asynchronous callbacks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native Mallabe API, this operation is `POST /websites/thumbnail` (base URL `https://mallabe.p.rapidapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-website-thumbnail.md) for the provider-specific parameters and requirements.

