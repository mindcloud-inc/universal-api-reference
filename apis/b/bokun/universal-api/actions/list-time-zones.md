# Bokun: List Time Zones

Retrieves supported time zones from Bokun.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-time-zones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-time-zones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-time-zones?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/timezones` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-zones.md) for the provider-specific parameters and requirements.

