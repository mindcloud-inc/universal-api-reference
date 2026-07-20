# Starshipit: Get Rates



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/get-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/get-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/get-rates?${params}`, {
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
| `sender.street` | string | no |  |
| `sender.suburb` | string | no |  |
| `sender.city` | string | no |  |
| `sender.state` | string | no |  |
| `sender.postCode` | string | no |  |
| `sender.countryCode` | string | no |  |
| `destination.street` | string | no |  |
| `destination.suburb` | string | no |  |
| `destination.city` | string | no |  |
| `destination.state` | string | no |  |
| `destination.postCode` | string | no |  |
| `destination.countryCode` | string | no |  |
| `packages[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rates": [
        {
          "serviceCode": "string",
          "serviceName": "Ava Chen",
          "totalPrice": 1
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rates` | array<object> |  |
| `rates[].serviceCode` | string |  |
| `rates[].serviceName` | string |  |
| `rates[].totalPrice` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `POST /rates` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rates.md) for the provider-specific parameters and requirements.

