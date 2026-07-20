# CampaignKit: Get Validation Job Results

Retrieves paginated validation job results from CampaignKit.

```
GET https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/get-validation-job-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CampaignKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/get-validation-job-results?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/get-validation-job-results?${params}`, {
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
| `id` | number | yes | Validation job ID. |
| `pos` | number | no | Starting position offset for result pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        [
          {}
        ]
      ],
      "filteredEntries": 1,
      "lastEntryId": 1,
      "totalEntries": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries[]` | array<object> |  |
| `entries[].email` | string |  |
| `entries[].result.classifier` | string |  |
| `entries[].result.description[]` | array<string> |  |
| `entries[].result.mailbox` | string |  |
| `entries[].result.mx` | string |  |
| `entries[].result.score` | number |  |
| `entries[].result.smtpResponse` | string |  |
| `entries[].result.syntax` | string |  |
| `filteredEntries` | number |  |
| `lastEntryId` | number |  |
| `totalEntries` | number |  |

## Native endpoint

Through the native CampaignKit API, this operation is `GET /v1/email/validate/job/{{id}}/result` (base URL `https://api.campaignkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-validation-job-results.md) for the provider-specific parameters and requirements.

