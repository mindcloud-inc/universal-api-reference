# The Guardian: Search Content

Finds content in The Guardian with optional search filters.

```
GET https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/search-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Guardian `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/search-content?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/search-content?${params}`, {
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
| `fromDate` | string | no | Return content published on or after this date. |
| `q` | string | no | Free-text query string used to search Guardian content. |
| `section` | string | no | Filter results to one or more Guardian sections. |
| `showBlocks` | string | no | Block expansion mode for each returned item. |
| `showElements` | string | no | When true, include element data in each result. |
| `showFields` | string | no | Comma-separated content field names to expand in each result. |
| `showReferences` | string | no | Reference expansion mode for each returned item. |
| `showSection` | string | no | When true, include section information in each result. |
| `showTags` | string | no | Tag expansion mode for each returned item. |
| `tag` | string | no | Filter results to one or more Guardian tags. |
| `toDate` | string | no | Return content published on or before this date. |
| `useDate` | string | no | Date field Guardian should use when applying from/to date filters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": "https://example.com",
      "fields": {
        "headline": "string",
        "trailText": "string"
      },
      "id": "string",
      "isHosted": true,
      "pillarId": "string",
      "pillarName": "Ava Chen",
      "sectionId": "string",
      "sectionName": "Ava Chen",
      "type": "string",
      "webPublicationDate": "string",
      "webTitle": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUrl` | string |  |
| `fields` | object |  |
| `fields.headline` | string |  |
| `fields.trailText` | string |  |
| `id` | string |  |
| `isHosted` | boolean |  |
| `pillarId` | string |  |
| `pillarName` | string |  |
| `sectionId` | string |  |
| `sectionName` | string |  |
| `type` | string |  |
| `webPublicationDate` | string |  |
| `webTitle` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native The Guardian API, this operation is `GET /search` (base URL `https://content.guardianapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-content.md) for the provider-specific parameters and requirements.

