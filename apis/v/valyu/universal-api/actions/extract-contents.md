# Valyu: Extract Contents



```
GET https://connect.mindcloud.co/v1/universal/valyu/latest/actions/extract-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Valyu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/valyu/latest/actions/extract-contents?connectionId=$CONNECTION_ID&urls%5B%5D=Add%20one%20or%20more%20HTTPS%20URLs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urls[]": "Add one or more HTTPS URLs"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/valyu/latest/actions/extract-contents?${params}`, {
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
| `urls[]` | array<string> | yes | URLs to extract content from. Example: `Add one or more HTTPS URLs`. |
| `response_length` | string | no | Maximum character length of extracted content per URL. Example: `short, medium, large, max, or a number`. |
| `extract_effort` | string | no | Controls how pages are rendered for extraction. |
| `summary` | string | no | Optional AI-powered content processing mode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "dataType": "string",
      "description": "string",
      "id": "string",
      "imageUrl": {},
      "length": 1,
      "price": 1,
      "publicationDate": "2026-05-07T12:00:00.000Z",
      "source": "string",
      "sourceType": "string",
      "status": "string",
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
| `content` | string |  |
| `dataType` | string |  |
| `description` | string |  |
| `id` | string |  |
| `imageUrl` | object |  |
| `length` | number |  |
| `price` | number |  |
| `publicationDate` | date |  |
| `source` | string |  |
| `sourceType` | string |  |
| `status` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Valyu API, this operation is `POST /contents` (base URL `https://api.valyu.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-contents.md) for the provider-specific parameters and requirements.

