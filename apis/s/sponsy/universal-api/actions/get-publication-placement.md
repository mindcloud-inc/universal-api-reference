# Sponsy: Get Publication Placement

Retrieves a publication placement from Sponsy.

```
GET https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/get-publication-placement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/get-publication-placement?connectionId=$CONNECTION_ID&publicationId=string&placementId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicationId": "string",
  "placementId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/get-publication-placement?${params}`, {
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
| `publicationId` | list<string> | yes | Publication ID from List Publications. |
| `placementId` | string | yes | Placement ID from List Publication Placements. |

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
      "externalIds": [
        "string"
      ],
      "id": "string",
      "isGroup": true,
      "isKit": true,
      "isPreviewEnabled": true,
      "name": "Ava Chen",
      "order": 1,
      "parentId": "string",
      "pipedriveProductIds": [
        "string"
      ],
      "placementHtml": "string",
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
| `externalIds` | array<string> | External placement identifiers. |
| `id` | string | Sponsy placement ID. |
| `isGroup` | boolean | Whether the placement groups child placements. |
| `isKit` | boolean | Whether the placement is a kit placement. |
| `isPreviewEnabled` | boolean | Whether placement preview is enabled. |
| `name` | string | Placement name. |
| `order` | number | Placement display order. |
| `parentId` | string | Parent placement ID when nested. |
| `pipedriveProductIds` | array<string> | Linked Pipedrive product IDs. |
| `placementHtml` | string | Placement HTML when configured. |
| `publicationId` | string | Parent publication ID. |
| `slug` | string | Placement slug. |
| `updatedAt` | date | Placement update timestamp. |

## Native endpoint

Through the native Sponsy API, this operation is `GET /v1/publications/:publicationId/placements/:placementId` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-publication-placement.md) for the provider-specific parameters and requirements.

