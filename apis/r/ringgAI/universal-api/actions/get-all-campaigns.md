# Ringg AI: Get All Campaigns

Retrieves campaigns from Ringg AI.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-all-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-all-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-all-campaigns?${params}`, {
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
| `callCount` | boolean | no | Whether to include call count for each campaign (default: true). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaigns": [
        {
          "campaignEndTime": "2026-05-07T12:00:00.000Z",
          "campaignStartTime": "2026-05-07T12:00:00.000Z",
          "campaignStatus": "string",
          "completedCount": 1,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "registeredCount": 1,
          "totalCount": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "pagination": {
        "limit": 1,
        "offset": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaigns` | array<object> |  |
| `campaigns[].campaignEndTime` | date | Scheduled end time for the campaign |
| `campaigns[].campaignStartTime` | date | Scheduled start time for the campaign |
| `campaigns[].campaignStatus` | string | Current status of the campaign |
| `campaigns[].completedCount` | number | Number of completed calls (only included when call_count=true) |
| `campaigns[].createdAt` | date | Campaign creation timestamp |
| `campaigns[].id` | string | Campaign unique identifier |
| `campaigns[].name` | string | Campaign name |
| `campaigns[].registeredCount` | number | Number of registered calls (only included when call_count=true) |
| `campaigns[].totalCount` | number | Total number of calls in campaign (only included when call_count=true) |
| `campaigns[].updatedAt` | date | Campaign last update timestamp |
| `pagination` | object |  |
| `pagination.limit` | number | Number of campaigns requested per page |
| `pagination.offset` | number | Number of campaigns skipped |
| `pagination.total` | number | Total number of campaigns available |

## Native endpoint

Through the native Ringg AI API, this operation is `GET /campaign/all` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-campaigns.md) for the provider-specific parameters and requirements.

