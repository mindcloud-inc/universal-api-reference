# Constant Contact: Get Email Campaign Summary Report

Retrieves an email campaign summary report from Constant Contact.

```
GET https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-email-campaign-summary-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-email-campaign-summary-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-email-campaign-summary-report?${params}`, {
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
| `limit` | number | no | Number of summary records per page (max 500). Example: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aggregatePercents": {},
      "bulkEmailCampaignSummaries": [
        {}
      ],
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregatePercents` | object | Aggregate click/open/bounce/unsubscribe rates for page results. |
| `bulkEmailCampaignSummaries` | array<object> | Collection of email campaign summary rows. |
| `links` | object | HAL pagination links when present. |

## Native endpoint

Through the native Constant Contact API, this operation is `GET /reports/summary_reports/email_campaign_summaries` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-campaign-summary-report.md) for the provider-specific parameters and requirements.

