# DMARC Report: Get Domain

Retrieves a domain from DMARC Report.

```
GET https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-domain?connectionId=$CONNECTION_ID&accountId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-domain?${params}`, {
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
| `id` | string | yes | Domain identifier from the endpoint path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "dmarcStatus": "string",
      "id": 1,
      "mtaStsReport": true,
      "mtaStsStatus": "string",
      "parkedDomain": true,
      "ruaReport": true,
      "rufReport": true,
      "slug": "string",
      "tags": [
        {}
      ],
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Domain address. |
| `dmarcStatus` | string | DMARC status for the domain. |
| `id` | number | Domain identifier. |
| `mtaStsReport` | boolean | Whether MTA-STS reporting is enabled. |
| `mtaStsStatus` | string | MTA-STS status for the domain. |
| `parkedDomain` | boolean | Whether the domain is parked. |
| `ruaReport` | boolean | Whether RUA aggregate reports are enabled. |
| `rufReport` | boolean | Whether RUF forensic reports are enabled. |
| `slug` | string | Domain slug. |
| `tags` | array<object> | Tag objects associated with the domain. |
| `userId` | number | Owner user identifier. |

## Native endpoint

Through the native DMARC Report API, this operation is `GET /accounts/:accountId/domains/:id.json` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain.md) for the provider-specific parameters and requirements.

