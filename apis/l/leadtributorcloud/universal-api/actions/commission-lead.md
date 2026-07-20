# leadtributor.cloud: Commission Lead

Creates a commission for a lead in leadtributor.cloud.

```
POST https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/commission-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a leadtributor.cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/commission-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "5df6897d-0962-4005-adba-12994a984a76",
  "salesPartnerId": "REQUIRED_SALES_PARTNER_ID",
  "salesPipelineId": "REQUIRED_SALES_PIPELINE_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/commission-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "5df6897d-0962-4005-adba-12994a984a76",
    "salesPartnerId": "REQUIRED_SALES_PARTNER_ID",
    "salesPipelineId": "REQUIRED_SALES_PIPELINE_ID"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadId` | string | yes | ID of the lead to commission. Default: `5df6897d-0962-4005-adba-12994a984a76`. |
| `salesPartnerId` | string | yes | Sales partner ID that should receive the lead commission. Default: `REQUIRED_SALES_PARTNER_ID`. |
| `salesPipelineId` | string | yes | Sales pipeline ID for the lead commission. Default: `REQUIRED_SALES_PIPELINE_ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commissionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commissionId` | string | ID of the created commission. |

## Native endpoint

Through the native leadtributor.cloud API, this operation is `POST /leads/:leadId/commissions` (base URL `https://api.leadtributor.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/commission-lead.md) for the provider-specific parameters and requirements.

