# PickFu: List Surveys



```
GET https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PickFu `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/list-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/list-surveys?${params}`, {
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
| `status` | string | no | Filter surveys by status. |
| `type` | string | no | Filter surveys by question type. |
| `optionType` | string | no | Filter surveys by option type. |
| `countries` | string | no | Filter surveys by country codes. Accepts multiple values in one string, delimited by `,`. |
| `tags` | string | no | Filter surveys by tag IDs. Accepts multiple values in one string, delimited by `,`. |
| `audiences` | string | no | Filter surveys by audience IDs. Accepts multiple values in one string, delimited by `,`. |
| `text` | string | no | Search survey names and questions. |
| `memberId` | string | no | Filter surveys by team member ID. Accepts multiple values in one string, delimited by `,`. |
| `projectIds` | string | no | Filter surveys by project IDs. Accepts multiple values in one string, delimited by `,`. |
| `publishedAfter` | date | no | Only include surveys published after this ISO 8601 datetime. |
| `sortBy` | string | no | Sort surveys by the selected field. |
| `dir` | string | no | Sort direction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorName": "Ava Chen",
      "elements": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "numResponses": 1,
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "sampleSize": 1,
      "status": "string",
      "targeting": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date |  |
| `countryCode` | string |  |
| `createdAt` | date |  |
| `creatorName` | string |  |
| `elements` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `numResponses` | number |  |
| `publishedAt` | date |  |
| `sampleSize` | number |  |
| `status` | string |  |
| `targeting` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native PickFu API, this operation is `GET /surveys` (base URL `https://api.pickfu.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

