# CampaignKit: Get Validation Job

Retrieves a validation job from CampaignKit by ID.

```
GET https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/get-validation-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CampaignKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/get-validation-job?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/get-validation-job?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailCount": 1,
      "file": "string",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "integration": {
        "id": 1,
        "system": "string"
      },
      "label": "string",
      "source": "string",
      "state": "string",
      "summary": {
        "deliverableCount": 1,
        "riskyCount": 1,
        "totalEmails": 1,
        "undeliverableCount": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `createdAt` | date |  |
| `emailCount` | number |  |
| `file` | string |  |
| `finishedAt` | date |  |
| `id` | number |  |
| `integration` | object |  |
| `integration.id` | number |  |
| `integration.system` | string |  |
| `label` | string |  |
| `source` | string |  |
| `state` | string |  |
| `summary` | object |  |
| `summary.deliverableCount` | number |  |
| `summary.riskyCount` | number |  |
| `summary.totalEmails` | number |  |
| `summary.undeliverableCount` | number |  |

## Native endpoint

Through the native CampaignKit API, this operation is `GET /v1/email/validate/job/{{id}}` (base URL `https://api.campaignkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-validation-job.md) for the provider-specific parameters and requirements.

