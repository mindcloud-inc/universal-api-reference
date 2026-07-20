# Refiner: List Responses

Retrieves survey views and responses from Refiner.

```
GET https://connect.mindcloud.co/v1/universal/refiner/latest/actions/list-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refiner `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/list-responses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refiner/latest/actions/list-responses?${params}`, {
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
| `formUuid` | string | no | Filter responses for one survey form UUID. |
| `formUuids[]` | array<string> | no | Filter responses for multiple survey form UUIDs. |
| `segmentUuid` | string | no | Filter responses for one segment UUID. |
| `segmentUuids[]` | array<string> | no | Filter responses for multiple segment UUIDs. |
| `dateRangeStart` | date | no | Return responses on or after this ISO 8601 timestamp. |
| `dateRangeEnd` | date | no | Return responses before this ISO 8601 timestamp. |
| `include` | string | no | Choose whether to return completed responses only, partials, or all survey views. |
| `search` | string | no | Match the contact user ID, Refiner UUID, email, or name. |
| `withAttributes` | boolean | no | Include all stored contact attributes on each response contact. |
| `pageCursor` | string | no | Cursor for the next response page returned by Refiner. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "contact": {},
      "data": {},
      "dismissedAt": "2026-05-07T12:00:00.000Z",
      "firstDataReceptionAt": "2026-05-07T12:00:00.000Z",
      "firstShownAt": "2026-05-07T12:00:00.000Z",
      "form": {},
      "lastDataReceptionAt": "2026-05-07T12:00:00.000Z",
      "lastShownAt": "2026-05-07T12:00:00.000Z",
      "receivedAt": "2026-05-07T12:00:00.000Z",
      "showCounter": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date |  |
| `contact` | object |  |
| `data` | object |  |
| `dismissedAt` | date |  |
| `firstDataReceptionAt` | date |  |
| `firstShownAt` | date |  |
| `form` | object |  |
| `lastDataReceptionAt` | date |  |
| `lastShownAt` | date |  |
| `receivedAt` | date |  |
| `showCounter` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Refiner API, this operation is `GET /responses` (base URL `https://api.refiner.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-responses.md) for the provider-specific parameters and requirements.

