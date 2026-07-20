# DMARC Report: Get Forensic Report

Retrieves a forensic report from DMARC Report.

```
GET https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-forensic-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-forensic-report?connectionId=$CONNECTION_ID&accountId=string&domainId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "domainId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-forensic-report?${params}`, {
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
| `id` | string | yes | Forensic report identifier from the endpoint path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "arrivalDate": "2026-05-07T12:00:00.000Z",
      "deliveryResult": "string",
      "domainId": 1,
      "feedbackType": "string",
      "fromAddress": "string",
      "id": 1,
      "ipAddress": {},
      "messageId": "string",
      "reportedDomain": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arrivalDate` | date | Message arrival date. |
| `deliveryResult` | string | Delivery result. |
| `domainId` | number | Domain identifier. |
| `feedbackType` | string | Feedback type. |
| `fromAddress` | string | Sender address. |
| `id` | number | Forensic report identifier. |
| `ipAddress` | object | IP address details for the report. |
| `messageId` | string | Message identifier. |
| `reportedDomain` | string | Reported domain. |
| `subject` | string | Message subject. |

## Native endpoint

Through the native DMARC Report API, this operation is `GET /accounts/:accountId/domains/:domainId/forensic_reports/:id.json` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-forensic-report.md) for the provider-specific parameters and requirements.

