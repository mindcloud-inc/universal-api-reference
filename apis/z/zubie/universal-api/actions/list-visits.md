# Zubie: List Visits

Retrieves visits from Zubie.

```
GET https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-visits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-visits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-visits?${params}`, {
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
      "entry_timestamp": "string",
      "exit_timestamp": "string",
      "key": "string",
      "place_key": "string",
      "status": "string",
      "vehicle_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entry_timestamp` | string |  |
| `exit_timestamp` | string |  |
| `key` | string |  |
| `place_key` | string |  |
| `status` | string |  |
| `vehicle_key` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `GET /places/visits` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-visits.md) for the provider-specific parameters and requirements.

