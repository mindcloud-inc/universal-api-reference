# CampaignKit: Create Validation Job

Creates a bulk email validation job in CampaignKit.

```
POST https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/create-validation-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CampaignKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/create-validation-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/create-validation-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `integration` | number | no | Integration ID when importing contacts from a connected service. |
| `label` | string | no | Descriptive label for the validation job. |
| `source` | string | yes | Source type for the validation job: input, file, or excel. One of: `0`, `1`, `2`. |
| `input` | string | no | Comma-separated or newline-separated email addresses when source is input. |
| `file` | file | no | CSV or Excel file when source is file or excel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Unique validation job ID. |

## Native endpoint

Through the native CampaignKit API, this operation is `POST /v1/email/validate/job` (base URL `https://api.campaignkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-validation-job.md) for the provider-specific parameters and requirements.

