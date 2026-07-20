# Ringg AI: Download Call History

Downloads call history from Ringg AI as CSV.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/download-call-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/download-call-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/download-call-history?${params}`, {
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
| `startDate` | date | no | Filter calls starting from this date (ISO 8601 format with timezone) |
| `endDate` | date | no | Filter calls up to this date (ISO 8601 format with timezone) |
| `agentId[]` | array<string> | no | Filter by agent ID(s) - can be repeated for multiple agents. |
| `status` | string | no | Filter by call status. |
| `includeAnalysis` | boolean | no | Include call analysis data (platform_analysis and client_analysis) in the export. |
| `callType` | string | no | Filter by call type. |
| `bulkListId` | string | no | Filter by bulk list ID. |
| `voicemail` | boolean | no | Filter by voicemail status. |
| `fromNumber` | string | no | Filter by caller phone number. |
| `toNumber` | string | no | Filter by callee phone number. |
| `callId` | string | no | Filter by specific call ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Success message when email format is used |

## Native endpoint

Through the native Ringg AI API, this operation is `POST /calling/history/download` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/download-call-history.md) for the provider-specific parameters and requirements.

