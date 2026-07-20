# UK Check VAT: Check VAT Registration



```
GET https://connect.mindcloud.co/v1/universal/uKCheckVAT/latest/actions/check-vat-registration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UK Check VAT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uKCheckVAT/latest/actions/check-vat-registration?connectionId=$CONNECTION_ID&targetVrn=553557881" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "targetVrn": "553557881"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uKCheckVAT/latest/actions/check-vat-registration?${params}`, {
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
| `targetVrn` | string | yes | UK VAT registration number to check. HMRC accepts a 9-digit or 12-digit number. Example: `553557881`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "processingDate": "2026-05-07T12:00:00.000Z",
      "target": {
        "address": {
          "countryCode": "string",
          "line1": "string",
          "postcode": "string"
        },
        "name": "Ava Chen",
        "vatNumber": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `processingDate` | date | Timestamp when HMRC processed the check. |
| `target` | object | VAT registered business returned by HMRC. |
| `target.address` | object | Registered business address. |
| `target.address.countryCode` | string | Registered address country code. |
| `target.address.line1` | string | First line of the registered address. |
| `target.address.postcode` | string | Registered address postcode. |
| `target.name` | string | Registered business name. |
| `target.vatNumber` | string | VAT registration number that HMRC matched. |

## Native endpoint

Through the native UK Check VAT API, this operation is `GET /organisations/vat/check-vat-number/lookup/:targetVrn` (base URL `https://test-api.service.hmrc.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-vat-registration.md) for the provider-specific parameters and requirements.

