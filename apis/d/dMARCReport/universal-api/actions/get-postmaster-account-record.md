# DMARC Report: Get Postmaster Account Record

Retrieves a postmaster account record from DMARC Report.

```
GET https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-postmaster-account-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-postmaster-account-record?connectionId=$CONNECTION_ID&id=string&email=ava%40example.com&item=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "email": "ava@example.com",
  "item": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-postmaster-account-record?${params}`, {
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
| `id` | string | yes | Postmaster account record identifier from the endpoint path. |
| `email` | string | yes | Email address of the connected Postmaster account. |
| `item` | string | yes | Domain for which Postmaster data is needed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticationData": {},
      "deliveryErrorsData": {},
      "domainReputationData": {},
      "encryptionData": {},
      "feedbackLoopData": {},
      "ipReputationData": {},
      "spamRateData": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticationData` | object | Authentication performance keyed by date. |
| `deliveryErrorsData` | object | Delivery error records keyed by date. |
| `domainReputationData` | object | Domain reputation data keyed by date. |
| `encryptionData` | object | Encryption metrics keyed by date. |
| `feedbackLoopData` | object | Feedback loop records keyed by date. |
| `ipReputationData` | object | IP reputation data keyed by date and reputation tier. |
| `spamRateData` | object | Spam rate data keyed by date. |

## Native endpoint

Through the native DMARC Report API, this operation is `GET /postmaster_account_records/:id.json` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-postmaster-account-record.md) for the provider-specific parameters and requirements.

