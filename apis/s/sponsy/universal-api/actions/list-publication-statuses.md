# Sponsy: List Publication Statuses

Retrieves publication statuses from Sponsy.

```
GET https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-publication-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-publication-statuses?connectionId=$CONNECTION_ID&limit=25&offset=0&publicationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "publicationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-publication-statuses?${params}`, {
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
| `publicationId` | list<string> | yes | Publication to list statuses for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "order": 1,
      "shapeCode": "string",
      "slug": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Status color. |
| `createdAt` | date | Status creation timestamp. |
| `deletedAt` | date | Deletion timestamp when present. |
| `id` | string | Sponsy status ID. |
| `name` | string | Status name. |
| `order` | number | Status display order. |
| `shapeCode` | string | Status shape code. |
| `slug` | string | Status slug. |
| `updatedAt` | date | Status update timestamp. |

## Native endpoint

Through the native Sponsy API, this operation is `GET /v1/publications/:publicationId/status` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-publication-statuses.md) for the provider-specific parameters and requirements.

