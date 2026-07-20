# IPInfo: Get Lite My IP Details



```
GET https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/get-lite-my-ip-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/get-lite-my-ip-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/get-lite-my-ip-details?${params}`, {
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
      "asDomain": "string",
      "asn": "string",
      "asName": "Ava Chen",
      "continent": "string",
      "continentCode": "string",
      "country": "string",
      "countryCode": "string",
      "ip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asDomain` | string |  |
| `asn` | string |  |
| `asName` | string |  |
| `continent` | string |  |
| `continentCode` | string |  |
| `country` | string |  |
| `countryCode` | string |  |
| `ip` | string |  |

## Native endpoint

Through the native IPInfo API, this operation is `GET /lite/me` (base URL `https://api.ipinfo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lite-my-ip-details.md) for the provider-specific parameters and requirements.

