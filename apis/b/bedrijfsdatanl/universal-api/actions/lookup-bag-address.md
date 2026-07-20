# Bedrijfsdata.nl: Lookup BAG Address



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-bag-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-bag-address?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-bag-address?${params}`, {
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
| `number` | string | no | House number for the postcode lookup. |
| `postcode` | string | no | Dutch postcode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bag": [
        {
          "addition": "string",
          "city": "string",
          "constructionYear": 1,
          "floorArea": 1,
          "freeformaddress": "string",
          "lat": 1,
          "letter": "string",
          "lon": 1,
          "municipality": "string",
          "number": "string",
          "postcode": "string",
          "province": "string",
          "provinceCode": "string",
          "purpose": "string",
          "street": "string"
        }
      ],
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "found": 1,
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
| `bag[].addition` | string |  |
| `bag[].city` | string |  |
| `bag[].constructionYear` | number |  |
| `bag[].floorArea` | number |  |
| `bag[].freeformaddress` | string |  |
| `bag[].lat` | number |  |
| `bag[].letter` | string |  |
| `bag[].lon` | number |  |
| `bag[].municipality` | string |  |
| `bag[].number` | string |  |
| `bag[].postcode` | string |  |
| `bag[].province` | string |  |
| `bag[].provinceCode` | string |  |
| `bag[].purpose` | string |  |
| `bag[].street` | string |  |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `found` | number |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /bag` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-bag-address.md) for the provider-specific parameters and requirements.

