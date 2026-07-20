# ipdata.co: Get Caller IP Details



```
GET https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ipdata.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-details?${params}`, {
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
      "asn": {},
      "calling_code": "string",
      "city": "string",
      "continent_code": "string",
      "continent_name": "Ava Chen",
      "count": "string",
      "country_code": "string",
      "country_name": "Ava Chen",
      "currency": {},
      "emoji_flag": "string",
      "emoji_unicode": "string",
      "flag": "string",
      "ip": "string",
      "is_eu": true,
      "languages": [
        {}
      ],
      "latitude": 1,
      "longitude": 1,
      "postal": "string",
      "region": "string",
      "region_code": "string",
      "region_type": "string",
      "threat": {},
      "time_zone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asn` | object |  |
| `calling_code` | string |  |
| `city` | string |  |
| `continent_code` | string |  |
| `continent_name` | string |  |
| `count` | string |  |
| `country_code` | string |  |
| `country_name` | string |  |
| `currency` | object |  |
| `emoji_flag` | string |  |
| `emoji_unicode` | string |  |
| `flag` | string |  |
| `ip` | string |  |
| `is_eu` | boolean |  |
| `languages` | array<object> |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `postal` | string |  |
| `region` | string |  |
| `region_code` | string |  |
| `region_type` | string |  |
| `threat` | object |  |
| `time_zone` | object |  |

## Native endpoint

Through the native ipdata.co API, this operation is `GET /` (base URL `https://api.ipdata.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-caller-ip-details.md) for the provider-specific parameters and requirements.

