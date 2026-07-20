# Bedrijfsdata.nl: Validate IBAN



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-iban
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-iban?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-iban?${params}`, {
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
| `iban` | string | no | IBAN to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "iban": {
        "country": "string",
        "countryCode": "string",
        "iban": "string",
        "ibanHuman": "string",
        "sepa": 1,
        "success": 1,
        "swift": 1,
        "verified": true,
        "verifiedChecksum": true
      },
      "monthlyCredits": 1,
      "product": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `iban.country` | string |  |
| `iban.countryCode` | string |  |
| `iban.iban` | string |  |
| `iban.ibanHuman` | string |  |
| `iban.sepa` | number |  |
| `iban.success` | number |  |
| `iban.swift` | number |  |
| `iban.verified` | boolean |  |
| `iban.verifiedChecksum` | boolean |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /iban` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-iban.md) for the provider-specific parameters and requirements.

