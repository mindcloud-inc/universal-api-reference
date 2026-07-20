# Bedrijfsdata.nl: Validate Phone



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-phone?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-phone?${params}`, {
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
| `phone` | string | no | Phone number to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "monthlyCredits": 1,
      "phone": {
        "carrier": "string",
        "country": "string",
        "int": "string",
        "international": "string",
        "ismobile": 1,
        "national": "string",
        "region": "string",
        "success": 1,
        "valid": 1,
        "wrongPhone": 1
      },
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
| `monthlyCredits` | number |  |
| `phone.carrier` | string |  |
| `phone.country` | string |  |
| `phone.int` | string |  |
| `phone.international` | string |  |
| `phone.ismobile` | number |  |
| `phone.national` | string |  |
| `phone.region` | string |  |
| `phone.success` | number |  |
| `phone.valid` | number |  |
| `phone.wrongPhone` | number |  |
| `product` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /phone` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-phone.md) for the provider-specific parameters and requirements.

