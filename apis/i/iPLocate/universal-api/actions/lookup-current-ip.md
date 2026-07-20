# IPLocate: Lookup Current IP



```
GET https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/lookup-current-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPLocate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/lookup-current-ip?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/lookup-current-ip?${params}`, {
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
      "abuse": {},
      "asn": {},
      "calling_code": "string",
      "city": "string",
      "company": {},
      "continent": "string",
      "country": "string",
      "country_code": "string",
      "currency_code": "string",
      "hosting": {},
      "ip": "string",
      "is_anycast": true,
      "is_eu": true,
      "is_satellite": true,
      "latitude": 1,
      "longitude": 1,
      "postal_code": "string",
      "privacy": {},
      "subdivision": "string",
      "time_zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abuse` | object |  |
| `asn` | object |  |
| `calling_code` | string |  |
| `city` | string |  |
| `company` | object |  |
| `continent` | string |  |
| `country` | string |  |
| `country_code` | string |  |
| `currency_code` | string |  |
| `hosting` | object |  |
| `ip` | string |  |
| `is_anycast` | boolean |  |
| `is_eu` | boolean |  |
| `is_satellite` | boolean |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `postal_code` | string |  |
| `privacy` | object |  |
| `subdivision` | string |  |
| `time_zone` | string |  |

## Native endpoint

Through the native IPLocate API, this operation is `GET /lookup/` (base URL `https://iplocate.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-current-ip.md) for the provider-specific parameters and requirements.

