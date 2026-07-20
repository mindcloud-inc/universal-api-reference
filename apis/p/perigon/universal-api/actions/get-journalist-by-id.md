# Perigon: Get Journalist By ID

Retrieves a journalist profile from Perigon by ID.

```
GET https://connect.mindcloud.co/v1/universal/perigon/latest/actions/get-journalist-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perigon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/get-journalist-by-id?connectionId=$CONNECTION_ID&id=journalist_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "journalist_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perigon/latest/actions/get-journalist-by-id?${params}`, {
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
| `id` | string | yes | Example: `journalist_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "fullName": "Ava Chen",
      "headline": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "locations": [
        "string"
      ],
      "name": "Ava Chen",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `fullName` | string |  |
| `headline` | string |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `locations` | array<string> |  |
| `name` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Perigon API, this operation is `GET /v1/journalists/{id}` (base URL `https://api.perigon.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-journalist-by-id.md) for the provider-specific parameters and requirements.

