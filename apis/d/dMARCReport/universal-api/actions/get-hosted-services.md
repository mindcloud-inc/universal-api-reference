# DMARC Report: Get Hosted Services

Retrieves hosted service status for a domain in DMARC Report.

```
GET https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-hosted-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-hosted-services?connectionId=$CONNECTION_ID&accountId=string&domainId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "domainId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-hosted-services?${params}`, {
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
      "dmarcStatus": "string",
      "domain": {},
      "hostedDmarc": true,
      "hostedMtaSts": true,
      "mtaStsStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dmarcStatus` | string | Hosted DMARC status when available. |
| `domain` | object | Domain-level hosted-service context when returned by the provider. |
| `hostedDmarc` | boolean | Whether hosted DMARC is enabled for the domain. |
| `hostedMtaSts` | boolean | Whether hosted MTA-STS is enabled for the domain. |
| `mtaStsStatus` | string | Hosted MTA-STS status when available. |

## Native endpoint

Through the native DMARC Report API, this operation is `GET /accounts/:accountId/domains/:domainId/hosted_services.json` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hosted-services.md) for the provider-specific parameters and requirements.

