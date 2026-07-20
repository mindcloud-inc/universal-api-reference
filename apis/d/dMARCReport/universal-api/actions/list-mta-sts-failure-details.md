# DMARC Report: List MTA-STS Failure Details

Retrieves MTA-STS failure details from DMARC Report.

```
GET https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/list-mta-sts-failure-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/list-mta-sts-failure-details?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=string&domainId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "string",
  "domainId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/list-mta-sts-failure-details?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "failureDetails": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failureDetails` | array<object> | MTA-STS failure detail rows for the domain. |

## Native endpoint

Through the native DMARC Report API, this operation is `GET /accounts/:accountId/domains/:domainId/mta_sts_reports/mta_failure_details.json` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-mta-sts-failure-details.md) for the provider-specific parameters and requirements.

