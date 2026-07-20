# Airlabs: List Time Zones

Retrieves time zone records from Airlabs.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-time-zones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-time-zones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-time-zones?${params}`, {
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
      "country_code": "string",
      "dst": 1,
      "gmt": 1,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_code` | string | Country ISO 2 code. |
| `dst` | number | Daylight saving offset. |
| `gmt` | number | GMT offset. |
| `timezone` | string | Timezone identifier. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /timezones` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-zones.md) for the provider-specific parameters and requirements.

