# Bedrijfsdata.nl: Validate VAT Number



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-vat-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-vat-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-vat-number?${params}`, {
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
| `vat` | string | no | VAT number to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "monthlyCredits": 1,
      "product": "string",
      "status": "string",
      "vatDetail": {
        "active": 1,
        "address": "string",
        "city": "string",
        "country": "string",
        "name": "Ava Chen",
        "postcode": "string",
        "responseDate": "2026-05-07T12:00:00.000Z",
        "vat": "string"
      }
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
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |
| `vatDetail.active` | number |  |
| `vatDetail.address` | string |  |
| `vatDetail.city` | string |  |
| `vatDetail.country` | string |  |
| `vatDetail.name` | string |  |
| `vatDetail.postcode` | string |  |
| `vatDetail.responseDate` | date |  |
| `vatDetail.vat` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /vat` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-vat-number.md) for the provider-specific parameters and requirements.

