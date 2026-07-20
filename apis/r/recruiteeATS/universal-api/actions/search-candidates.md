# Recruitee ATS: Search Candidates



```
GET https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/search-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recruitee ATS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/search-candidates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/search-candidates?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filtersJson` | string | no | Array of filters serialized to a JSON string, as documented by Recruitee. |
| `sortBy` | string | no | Sort order with _asc or _desc suffix, for example created_at_desc. Default: `created_at_desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminId": {},
      "companyId": 1,
      "createdAt": "string",
      "deleted": true,
      "deletedAt": {},
      "deletedBy": {},
      "deletedByName": {},
      "emails": [
        "ava@example.com"
      ],
      "example": true,
      "gdprConsentEverGiven": {},
      "gdprExpiresAt": {},
      "gdprStatus": {},
      "gdprUncompletedChangeRequestCreatedAt": {},
      "gdprUncompletedRemovalRequestCreatedAt": {},
      "hasAvatar": true,
      "highlight": {},
      "id": 1,
      "initials": "string",
      "isAnonymous": true,
      "lastActivityAt": "string",
      "name": "Ava Chen",
      "new": true,
      "phones": [
        "string"
      ],
      "photoThumbUrl": "https://example.com",
      "placements": [
        {
          "candidateId": 1,
          "disqualified": true,
          "disqualifiedAt": {},
          "disqualifiedBy": {},
          "disqualifiedByName": {},
          "disqualifyKind": {},
          "disqualifyReason": {},
          "eeoDataStatus": {},
          "hiredAt": {},
          "id": 1,
          "isHired": true,
          "jobStartsAt": {},
          "offer": {
            "id": 1,
            "kind": "string",
            "slug": "string",
            "status": "string",
            "title": "string"
          },
          "overdueAt": {},
          "overdueDiff": {},
          "positiveRatings": {},
          "ratingVisible": true,
          "screeningScore": {},
          "stage": {}
        }
      ],
      "positiveRatings": 1,
      "ratingVisible": true,
      "softDeletedAt": {},
      "source": "string",
      "sources": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "tags": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "unreadNotifications": true,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminId` | object |  |
| `companyId` | number |  |
| `createdAt` | string |  |
| `deleted` | boolean |  |
| `deletedAt` | object |  |
| `deletedBy` | object |  |
| `deletedByName` | object |  |
| `emails[]` | string |  |
| `example` | boolean |  |
| `gdprConsentEverGiven` | object |  |
| `gdprExpiresAt` | object |  |
| `gdprStatus` | object |  |
| `gdprUncompletedChangeRequestCreatedAt` | object |  |
| `gdprUncompletedRemovalRequestCreatedAt` | object |  |
| `hasAvatar` | boolean |  |
| `highlight` | object |  |
| `id` | number |  |
| `initials` | string |  |
| `isAnonymous` | boolean |  |
| `lastActivityAt` | string |  |
| `name` | string |  |
| `new` | boolean |  |
| `phones[]` | string |  |
| `photoThumbUrl` | string |  |
| `placements[].candidateId` | number |  |
| `placements[].disqualified` | boolean |  |
| `placements[].disqualifiedAt` | object |  |
| `placements[].disqualifiedBy` | object |  |
| `placements[].disqualifiedByName` | object |  |
| `placements[].disqualifyKind` | object |  |
| `placements[].disqualifyReason` | object |  |
| `placements[].eeoDataStatus` | object |  |
| `placements[].hiredAt` | object |  |
| `placements[].id` | number |  |
| `placements[].isHired` | boolean |  |
| `placements[].jobStartsAt` | object |  |
| `placements[].offer.id` | number |  |
| `placements[].offer.kind` | string |  |
| `placements[].offer.slug` | string |  |
| `placements[].offer.status` | string |  |
| `placements[].offer.title` | string |  |
| `placements[].overdueAt` | object |  |
| `placements[].overdueDiff` | object |  |
| `placements[].positiveRatings` | object |  |
| `placements[].ratingVisible` | boolean |  |
| `placements[].screeningScore` | object |  |
| `placements[].stage` | object |  |
| `positiveRatings` | number |  |
| `ratingVisible` | boolean |  |
| `softDeletedAt` | object |  |
| `source` | string |  |
| `sources[].id` | number |  |
| `sources[].name` | string |  |
| `tags[].id` | number |  |
| `tags[].name` | string |  |
| `unreadNotifications` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Recruitee ATS API, this operation is `GET /c/:company_id/search/new/candidates` (base URL `https://api.recruitee.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-candidates.md) for the provider-specific parameters and requirements.

