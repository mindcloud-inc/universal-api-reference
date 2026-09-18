# Paycom: List Locations



```
GET https://connect.mindcloud.co/v1/universal/paycom/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycom `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycom/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycom/latest/actions/list-locations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "country": "string",
      "description": "string",
      "eEOCUnitNumber": "string",
      "facilityId": "string",
      "hiringSite": true,
      "locationHidden": true,
      "locationid": 1,
      "state": "string",
      "vETS4212HiringLocation": true,
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `country` | string |  |
| `description` | string |  |
| `eEOCUnitNumber` | string |  |
| `facilityId` | string |  |
| `hiringSite` | boolean |  |
| `locationHidden` | boolean |  |
| `locationid` | number |  |
| `state` | string |  |
| `vETS4212HiringLocation` | boolean |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Paycom API, this operation is `GET api/v1/cl/locations` (base URL `https://api.paycomonline.net/v4/rest/index.php/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

