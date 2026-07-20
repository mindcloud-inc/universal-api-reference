# Typlog: Get Site

Retrieves a Typlog site by ID.

```
GET https://connect.mindcloud.co/v1/universal/typlog/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typlog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typlog/latest/actions/get-site?connectionId=$CONNECTION_ID&id=4863" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "4863"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typlog/latest/actions/get-site?${params}`, {
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
| `id` | number | yes | Typlog site ID. Example: `4863`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "favicon": "string",
      "id": 1,
      "isAdmin": true,
      "languages": [
        "string"
      ],
      "name": "Ava Chen",
      "primaryLang": "string",
      "slug": "string",
      "status": "string",
      "summary": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": 1,
      "zoneinfo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseUrl` | string | Base URL for the site |
| `createdAt` | date | Site creation timestamp |
| `domain` | string | Custom domain for the site |
| `favicon` | string | Favicon URL |
| `id` | number | Typlog site ID |
| `isAdmin` | boolean | Whether the current account is an admin on the site |
| `languages` | array<string> | Configured site languages |
| `name` | string | Site display name |
| `primaryLang` | string | Primary site language |
| `slug` | string | Site slug |
| `status` | string | Site status |
| `summary` | string | Site summary or subtitle |
| `updatedAt` | date | Site last update timestamp |
| `user` | number | Owning Typlog user ID |
| `zoneinfo` | string | Site timezone |

## Native endpoint

Through the native Typlog API, this operation is `GET /sites/[:id]` (base URL `https://api.typlog.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

