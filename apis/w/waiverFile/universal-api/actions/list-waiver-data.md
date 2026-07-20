# WaiverFile: List Waiver Data

Retrieves waiver data from WaiverFile.

```
GET https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-waiver-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-waiver-data?connectionId=$CONNECTION_ID&limit=25&offset=0&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z&includeCustomColumns=true&consolidateParticipants=true&pageIndex=1&pageSize=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z",
  "includeCustomColumns": "true",
  "consolidateParticipants": "true",
  "pageIndex": "1",
  "pageSize": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-waiver-data?${params}`, {
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
| `startDate` | date | yes |  |
| `endDate` | date | yes |  |
| `includeCustomColumns` | boolean | yes |  |
| `consolidateParticipants` | boolean | yes |  |
| `pageIndex` | number | yes |  |
| `pageSize` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Table": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Table` | array<object> |  |

## Native endpoint

Through the native WaiverFile API, this operation is `GET /GetWaiverData` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-waiver-data.md) for the provider-specific parameters and requirements.

