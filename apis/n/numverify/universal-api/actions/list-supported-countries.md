# Numverify: List Supported Countries

Retrieves supported countries and dialing codes from Numverify.

```
GET https://connect.mindcloud.co/v1/universal/numverify/latest/actions/list-supported-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Numverify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/numverify/latest/actions/list-supported-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/numverify/latest/actions/list-supported-countries?${params}`, {
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
      "countryCode": "string",
      "countryName": "Ava Chen",
      "diallingCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryCode` | string |  |
| `countryName` | string |  |
| `diallingCode` | string |  |

## Native endpoint

Through the native Numverify API, this operation is `GET /countries` (base URL `https://apilayer.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-countries.md) for the provider-specific parameters and requirements.

