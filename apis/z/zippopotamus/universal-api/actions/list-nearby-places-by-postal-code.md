# Zippopotamus: List Nearby Places by Postal Code

Retrieves nearby places in Zippopotamus by postal code.

```
GET https://connect.mindcloud.co/v1/universal/zippopotamus/latest/actions/list-nearby-places-by-postal-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zippopotamus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zippopotamus/latest/actions/list-nearby-places-by-postal-code?connectionId=$CONNECTION_ID&country=US&postalcode=90210" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "US",
  "postalcode": "90210"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zippopotamus/latest/actions/list-nearby-places-by-postal-code?${params}`, {
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
| `country` | string | yes | ISO 3166-1 alpha-2 country code, such as US. Example: `US`. |
| `postalcode` | string | yes | Postal code used as the center point for nearby places, such as 90210. Example: `90210`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "near latitude": 1,
      "near longitude": 1,
      "nearby": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `near latitude` | number |  |
| `near longitude` | number |  |
| `nearby` | array<object> |  |

## Native endpoint

Through the native Zippopotamus API, this operation is `GET /nearby/{{country}}/{{postalcode}}` (base URL `https://api.zippopotam.us`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-nearby-places-by-postal-code.md) for the provider-specific parameters and requirements.

