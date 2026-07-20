# API Labz: IBAN Validator

Validates an IBAN with API Labz.

```
GET https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/iban-validator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a API Labz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/iban-validator?connectionId=$CONNECTION_ID&iban=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "iban": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/iban-validator?${params}`, {
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
| `iban` | string | yes | IBAN to validate |

## Response

```json
{
  "success": true,
  "data": [
    {
      "iban": "string",
      "isValid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `iban` | string |  |
| `isValid` | boolean |  |

## Native endpoint

Through the native API Labz API, this operation is `POST /module/113` (base URL `https://hub.apilabz.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/iban-validator.md) for the provider-specific parameters and requirements.

