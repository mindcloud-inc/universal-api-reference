# DMARC Report: Get Account Domain

Retrieves a domain account from DMARC Report.

```
GET https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-account-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-account-domain?connectionId=$CONNECTION_ID&accountId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-account-domain?${params}`, {
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
| `id` | string | yes | Account domain identifier from the endpoint path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "domainId": 1,
      "id": 1,
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | Account identifier on the account-domain record. |
| `domainId` | number | Domain identifier on the account-domain record. |
| `id` | number | Account-domain record identifier. |
| `timestamp` | string | Timestamp returned by DMARC Report for the account-domain record. |

## Native endpoint

Through the native DMARC Report API, this operation is `GET /accounts/:accountId/domain_accounts/:id` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-domain.md) for the provider-specific parameters and requirements.

