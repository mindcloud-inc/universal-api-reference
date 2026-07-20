# Bika.ai: List Embed Links

Retrieves embed links from a Bika.ai space.

```
GET https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-embed-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bika.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-embed-links?connectionId=$CONNECTION_ID&spaceId=spcfaZbYtV5hkHSLrDOqY4ve" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "spcfaZbYtV5hkHSLrDOqY4ve"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-embed-links?${params}`, {
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
| `spaceId` | string | yes | Bika.ai space ID. Example: `spcfaZbYtV5hkHSLrDOqY4ve`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "url": "https://example.com"
        }
      ],
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | array<object> |  |
| `data[].createdAt` | date |  |
| `data[].id` | string |  |
| `data[].name` | string |  |
| `data[].url` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Bika.ai API, this operation is `GET /spaces/:spaceId/embed-links` (base URL `https://bika.ai/api/openapi/bika/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-embed-links.md) for the provider-specific parameters and requirements.

