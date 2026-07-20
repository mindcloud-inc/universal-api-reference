# Bland AI: List Calls

Retrieves calls from your Bland AI account.

```
GET https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/list-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bland AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/list-calls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/list-calls?${params}`, {
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
| `fromNumber` | string | no |  |
| `toNumber` | string | no |  |
| `from` | number | no |  |
| `to` | number | no |  |
| `limit` | number | no |  |
| `ascending` | boolean | no |  |
| `sortBy` | string | no |  |
| `startDate` | string | no |  |
| `endDate` | string | no |  |
| `createdAt` | string | no |  |
| `timezone` | string | no |  |
| `updateStartDate` | string | no |  |
| `updateEndDate` | string | no |  |
| `completed` | boolean | no |  |
| `batchId` | string | no |  |
| `answeredBy` | string | no |  |
| `inbound` | boolean | no |  |
| `durationGt` | number | no |  |
| `durationLt` | number | no |  |
| `campaignId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calls": [
        {}
      ],
      "count": 1,
      "status": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calls` | array<object> |  |
| `count` | number |  |
| `status` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Bland AI API, this operation is `GET /v1/calls` (base URL `https://api.bland.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calls.md) for the provider-specific parameters and requirements.

