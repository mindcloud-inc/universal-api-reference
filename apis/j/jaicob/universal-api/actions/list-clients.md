# Jaicob: List Clients



```
GET https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaicob `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/list-clients?${params}`, {
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
| `query` | string | no | Optional client search text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "bannerImage": "string",
      "companyName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "details": {},
      "id": "string",
      "locations": [
        {}
      ],
      "ownerLocations": [
        {}
      ],
      "slug": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `bannerImage` | string |  |
| `companyName` | string |  |
| `createdAt` | date |  |
| `details` | object |  |
| `id` | string |  |
| `locations` | array<object> |  |
| `ownerLocations` | array<object> |  |
| `slug` | string |  |
| `updatedAt` | date |  |
| `website` | string |  |

## Native endpoint

Through the native Jaicob API, this operation is `GET /clients/public` (base URL `https://api.jaicob.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

