# Myphoner: List Leads in List

Retrieves leads from a list in Myphoner.

```
GET https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/list-leads-in-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Myphoner `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/list-leads-in-list?connectionId=$CONNECTION_ID&limit=25&offset=0&listId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "listId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/list-leads-in-list?${params}`, {
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
| `listId` | number | yes | The Myphoner list ID. |
| `order` | string | no | Use last_updated_first to return the most recently updated leads first. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "claimedAt": "2026-05-07T12:00:00.000Z",
      "claimedBy": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "detectedDuplicates": [
        1
      ],
      "id": 1,
      "ignoredDuplicates": [
        1
      ],
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "leadData": {},
      "listLocation": "string",
      "listName": "Ava Chen",
      "location": "string",
      "primaryIdentifier": "string",
      "scheduledFor": "2026-05-07T12:00:00.000Z",
      "secondaryIdentifier": "string",
      "state": "string",
      "tertiaryIdentifier": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `claimedAt` | date |  |
| `claimedBy` | string |  |
| `createdAt` | date |  |
| `detectedDuplicates` | array<number> |  |
| `id` | number |  |
| `ignoredDuplicates` | array<number> |  |
| `lastUpdated` | date |  |
| `leadData` | object |  |
| `listLocation` | string |  |
| `listName` | string |  |
| `location` | string |  |
| `primaryIdentifier` | string |  |
| `scheduledFor` | date |  |
| `secondaryIdentifier` | string |  |
| `state` | string |  |
| `tertiaryIdentifier` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Myphoner API, this operation is `GET /lists/:listId/leads` (base URL `https://{{credentials.subdomain}}.myphoner.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-leads-in-list.md) for the provider-specific parameters and requirements.

