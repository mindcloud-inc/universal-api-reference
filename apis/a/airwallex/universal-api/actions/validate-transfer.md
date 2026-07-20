# Airwallex: Validate Transfer

Validates transfer details in Airwallex before payout creation.

```
GET https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/validate-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airwallex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/validate-transfer?connectionId=$CONNECTION_ID&beneficiaryId=string&transferAmount=string&transferCurrency=string&transferMethod=string&reason=string&reference=string&requestId=string&sourceCurrency=string&lockRateOnCreate=true&transferDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "beneficiaryId": "string",
  "transferAmount": "string",
  "transferCurrency": "string",
  "transferMethod": "string",
  "reason": "string",
  "reference": "string",
  "requestId": "string",
  "sourceCurrency": "string",
  "lockRateOnCreate": "true",
  "transferDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/validate-transfer?${params}`, {
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
| `beneficiaryId` | string | yes | The saved Airwallex beneficiary ID to validate. |
| `transferAmount` | string | yes | The amount to validate for payout. |
| `transferCurrency` | string | yes | The payout currency, such as USD. |
| `transferMethod` | string | yes | The payout transfer method, such as LOCAL. |
| `reason` | string | yes | The transfer purpose or payout reason. |
| `reference` | string | yes | A transfer reference visible to the payer. |
| `requestId` | string | yes | A unique idempotency key for the validation request. |
| `sourceCurrency` | string | yes | The source wallet currency used to fund the payout. |
| `lockRateOnCreate` | boolean | yes | Whether to lock the FX rate at validation time. |
| `transferDate` | string | yes | The scheduled transfer date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Validation result returned by Airwallex, typically OK when the transfer request is valid. |

## Native endpoint

Through the native Airwallex API, this operation is `POST /api/v1/transfers/validate` (base URL `https://api-demo.airwallex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-transfer.md) for the provider-specific parameters and requirements.

