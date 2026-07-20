# Cursion: Get Page

Retrieves an existing page from Cursion.

```
GET https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-page?connectionId=$CONNECTION_ID&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-page?${params}`, {
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
| `pageId` | string | yes | The page identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "id": "string",
      "info": {},
      "page_url": "https://example.com",
      "site": "string",
      "tags": [
        "string"
      ],
      "time_created": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `id` | string |  |
| `info` | object |  |
| `page_url` | string |  |
| `site` | string |  |
| `tags` | array<string> |  |
| `time_created` | string |  |
| `user` | string |  |

## Native endpoint

Through the native Cursion API, this operation is `GET /page/{{pageId}}` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page.md) for the provider-specific parameters and requirements.

