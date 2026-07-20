# Sponsy: List Publication Placements

Retrieves publication placements from Sponsy.

```
GET https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-publication-placements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-publication-placements?connectionId=$CONNECTION_ID&limit=25&offset=0&publicationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "publicationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-publication-placements?${params}`, {
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
| `publicationId` | list<string> | yes | Publication to list placements for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "days": [
        "string"
      ],
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isGroup": true,
      "isKit": true,
      "name": "Ava Chen",
      "order": 1,
      "publicationId": "string",
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
| `archivedAt` | date | Archive timestamp when present. |
| `color` | string | Placement color when configured. |
| `createdAt` | date | Placement creation timestamp. |
| `days` | array<string> | Publication weekdays associated with the placement. |
| `deletedAt` | date | Deletion timestamp when present. |
| `id` | string | Sponsy placement ID. |
| `isGroup` | boolean | Whether the placement groups child placements. |
| `isKit` | boolean | Whether the placement is a kit placement. |
| `name` | string | Placement name. |
| `order` | number | Placement display order. |
| `publicationId` | string | Parent publication ID. |
| `slug` | string | Placement slug. |
| `updatedAt` | date | Placement update timestamp. |

## Native endpoint

Through the native Sponsy API, this operation is `GET /v1/publications/:publicationId/placements` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-publication-placements.md) for the provider-specific parameters and requirements.

