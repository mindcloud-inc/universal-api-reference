# CampaignKit: Download Validation Job Results

Downloads validation job results from CampaignKit as a CSV file.

```
GET https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/download-validation-job-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CampaignKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/download-validation-job-results?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/download-validation-job-results?${params}`, {
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
| `filters[]` | array<string> | no | Optional classifiers to include in the CSV download. |
| `id` | number | yes | Validation job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          1
        ]
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
| `data[]` | array<number> |  |
| `type` | string |  |

## Native endpoint

Through the native CampaignKit API, this operation is `GET /v1/email/validate/job/{{id}}/download` (base URL `https://api.campaignkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-validation-job-results.md) for the provider-specific parameters and requirements.

