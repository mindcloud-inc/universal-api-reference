# 44API: Validate VAT Number

Validates a VAT number with 44API and returns company details.

```
GET https://connect.mindcloud.co/v1/universal/aPI/latest/actions/validate-vat-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 44API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPI/latest/actions/validate-vat-number?connectionId=$CONNECTION_ID&vatNumber=string&countryCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vatNumber": "string",
  "countryCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aPI/latest/actions/validate-vat-number?${params}`, {
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
| `vatNumber` | string | yes | VAT number with or without country prefix. |
| `countryCode` | string | yes | ISO 2-letter country code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cachedAt": "2026-05-07T12:00:00.000Z",
      "company": {
        "address": "string",
        "name": "Ava Chen"
      },
      "countryCode": "string",
      "valid": true,
      "vatNumber": "string",
      "verificationDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cachedAt` | date |  |
| `company` | object |  |
| `company.address` | string |  |
| `company.name` | string |  |
| `countryCode` | string |  |
| `valid` | boolean |  |
| `vatNumber` | string |  |
| `verificationDate` | date |  |

## Native endpoint

Through the native 44API API, this operation is `POST /webhook/validate-vat` (base URL `https://api.44api.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-vat-number.md) for the provider-specific parameters and requirements.

