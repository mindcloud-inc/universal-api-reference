# UK Check VAT: Check VAT Registration With Reference Number



```
GET https://connect.mindcloud.co/v1/universal/uKCheckVAT/latest/actions/check-vat-registration-with-reference-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UK Check VAT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uKCheckVAT/latest/actions/check-vat-registration-with-reference-number?connectionId=$CONNECTION_ID&targetVrn=553557881&requesterVrn=146295999727" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "targetVrn": "553557881",
  "requesterVrn": "146295999727"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uKCheckVAT/latest/actions/check-vat-registration-with-reference-number?${params}`, {
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
| `requesterVrn` | string | yes | Your VAT registration number. HMRC accepts a 9-digit or 12-digit number and returns a consultation number when this requester is valid. Example: `146295999727`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "consultationNumber": "string",
      "processingDate": "2026-05-07T12:00:00.000Z",
      "requester": "string",
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
| `consultationNumber` | string | HMRC reference proving the VAT number check was made. |
| `processingDate` | date | Timestamp when HMRC processed the check. |
| `requester` | string | Requester VAT registration number used for the verified check. |
| `target` | object | VAT registered business returned by HMRC. |
| `target.address` | object | Registered business address. |
| `target.address.countryCode` | string | Registered address country code. |
| `target.address.line1` | string | First line of the registered address. |
| `target.address.postcode` | string | Registered address postcode. |
| `target.name` | string | Registered business name. |
| `target.vatNumber` | string | VAT registration number that HMRC matched. |

## Native endpoint

Through the native UK Check VAT API, this operation is `GET /organisations/vat/check-vat-number/lookup/:targetVrn/:requesterVrn` (base URL `https://test-api.service.hmrc.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-vat-registration-with-reference-number.md) for the provider-specific parameters and requirements.

