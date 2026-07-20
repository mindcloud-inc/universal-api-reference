# API Labz: VAT Validator

Validates a VAT number with API Labz.

```
GET https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/vat-validator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a API Labz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/vat-validator?connectionId=$CONNECTION_ID&vatNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vatNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/vat-validator?${params}`, {
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
| `vatNumber` | string | yes | VAT number to validate |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "address": "string",
        "name": "Ava Chen"
      },
      "country": {
        "code": "string",
        "name": "Ava Chen"
      },
      "valid": true,
      "vatNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.address` | string |  |
| `company.name` | string |  |
| `country.code` | string |  |
| `country.name` | string |  |
| `valid` | boolean |  |
| `vatNumber` | string |  |

## Native endpoint

Through the native API Labz API, this operation is `POST /module/114` (base URL `https://hub.apilabz.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/vat-validator.md) for the provider-specific parameters and requirements.

