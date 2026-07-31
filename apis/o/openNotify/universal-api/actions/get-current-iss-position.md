# Open Notify: Get Current ISS Position



```
GET https://connect.mindcloud.co/v1/universal/openNotify/latest/actions/get-current-iss-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Notify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openNotify/latest/actions/get-current-iss-position?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openNotify/latest/actions/get-current-iss-position?${params}`, {
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
      "iss_position": {},
      "message": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `iss_position` | object | ISS latitude and longitude, preserved as provider strings. |
| `message` | string | Provider operation status. |
| `timestamp` | number | Unix timestamp for the reported position. |

## Native endpoint

Through the native Open Notify API, this operation is `GET /iss-now.json` (base URL `http://api.open-notify.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-iss-position.md) for the provider-specific parameters and requirements.

