# DMARC Report: Get MTA-STS Report

Retrieves an MTA-STS report from DMARC Report.

```
GET https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-mta-sts-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-mta-sts-report?connectionId=$CONNECTION_ID&accountId=string&domainId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "domainId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-mta-sts-report?${params}`, {
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
| `id` | string | yes | MTA-STS report identifier from the endpoint path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domainId": 1,
      "failureDetails": [
        {}
      ],
      "id": 1,
      "organizationName": "Ava Chen",
      "policyDomain": "string",
      "policyType": "string",
      "reportId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domainId` | number | Domain identifier. |
| `failureDetails` | array<object> | Failure details included with the MTA-STS report. |
| `id` | number | MTA-STS report identifier. |
| `organizationName` | string | Reporting organization. |
| `policyDomain` | string | Policy domain. |
| `policyType` | string | MTA-STS policy type. |
| `reportId` | string | Provider report identifier. |

## Native endpoint

Through the native DMARC Report API, this operation is `GET /accounts/:accountId/domains/:domainId/mta_sts_reports/:id.json` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mta-sts-report.md) for the provider-specific parameters and requirements.

