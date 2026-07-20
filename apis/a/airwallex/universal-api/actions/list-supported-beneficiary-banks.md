# Airwallex: List Supported Beneficiary Banks

Retrieves supported beneficiary banks from Airwallex.

```
GET https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/list-supported-beneficiary-banks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airwallex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/list-supported-beneficiary-banks?connectionId=$CONNECTION_ID&bankCountryCode=string&accountCurrency=string&transferMethod=string&entityType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bankCountryCode": "string",
  "accountCurrency": "string",
  "transferMethod": "string",
  "entityType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/list-supported-beneficiary-banks?${params}`, {
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
| `bankCountryCode` | string | yes | The beneficiary bank country code, such as US. |
| `keyword` | string | no | Search keyword for supported financial institutions, minimum 3 characters. |
| `accountCurrency` | string | yes | The beneficiary account currency, such as USD. |
| `transferMethod` | string | yes | The payout transfer method, such as LOCAL or SWIFT. |
| `entityType` | string | yes | The beneficiary entity type, such as PERSONAL or COMPANY. |
| `localClearingSystem` | string | no | Optional local clearing system, such as ACH. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string | Human-readable beneficiary bank name. |
| `value` | string | Provider bank identifier or routing code value. |

## Native endpoint

Through the native Airwallex API, this operation is `GET /api/v1/beneficiary_form_schemas/supported_financial_institutions` (base URL `https://api-demo.airwallex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-beneficiary-banks.md) for the provider-specific parameters and requirements.

