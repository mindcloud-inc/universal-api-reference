# Bedrijfsdata.nl: Lookup Postcode



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-postcode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-postcode?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-postcode?${params}`, {
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
| `countryCode` | string | no | ISO2 country code. |
| `postcode` | string | no | Postcode to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "found": 1,
      "message": "string",
      "monthlyCredits": 1,
      "postcode": [
        {
          "admin1": "string",
          "admin2": "string",
          "admin3": {},
          "city": "string",
          "lat": 1,
          "lon": 1,
          "postcode": "string"
        }
      ],
      "product": "string",
      "status": "string",
      "success": 1,
      "wrongPostcode": 1
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
| `found` | number |  |
| `message` | string |  |
| `monthlyCredits` | number |  |
| `postcode[].admin1` | string |  |
| `postcode[].admin2` | string |  |
| `postcode[].admin3` | object |  |
| `postcode[].city` | string |  |
| `postcode[].lat` | number |  |
| `postcode[].lon` | number |  |
| `postcode[].postcode` | string |  |
| `product` | string |  |
| `status` | string |  |
| `success` | number |  |
| `wrongPostcode` | number |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /postcode` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-postcode.md) for the provider-specific parameters and requirements.

