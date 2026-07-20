# DMARC Report: Get Aggregate Report

Retrieves an aggregate report from DMARC Report.

```
GET https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-aggregate-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-aggregate-report?connectionId=$CONNECTION_ID&accountId=string&domainId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "domainId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-aggregate-report?${params}`, {
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
| `accountId` | string | yes | DMARC Report account identifier from the endpoint path. |
| `domainId` | string | yes | Domain identifier from the endpoint path. |
| `id` | string | yes | Aggregate report identifier from the endpoint path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateBegin": "2026-05-07T12:00:00.000Z",
      "dateEnd": "2026-05-07T12:00:00.000Z",
      "domainPolicy": "string",
      "email": "ava@example.com",
      "id": 1,
      "orgName": "Ava Chen",
      "policyDomain": "string",
      "recordsCount": 1,
      "reportId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateBegin` | date | Report date range start. |
| `dateEnd` | date | Report date range end. |
| `domainPolicy` | string | Published domain policy. |
| `email` | string | Reporter email. |
| `id` | number | Aggregate report identifier. |
| `orgName` | string | Reporting organization name. |
| `policyDomain` | string | Policy domain. |
| `recordsCount` | number | Number of aggregate records when provided. |
| `reportId` | string | Provider report identifier. |

## Native endpoint

Through the native DMARC Report API, this operation is `GET /accounts/:accountId/domains/:domainId/agg_reports/:id.json` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-aggregate-report.md) for the provider-specific parameters and requirements.

