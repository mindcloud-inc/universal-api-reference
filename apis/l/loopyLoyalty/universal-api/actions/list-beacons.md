# Loopy Loyalty: List Beacons



```
GET https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-beacons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-beacons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-beacons?${params}`, {
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
      "value": {
        "id": "string",
        "major": 1,
        "minor": 1,
        "name": "Ava Chen",
        "relevantText": "string",
        "uid": "string",
        "uuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value.id` | string | Beacon ID. |
| `value.major` | number | Beacon major value. |
| `value.minor` | number | Beacon minor value. |
| `value.name` | string | Beacon name. |
| `value.relevantText` | string | Lock-screen message shown when in range. |
| `value.uid` | string | Owner user ID. |
| `value.uuid` | string | Beacon UUID. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `GET /beacons` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-beacons.md) for the provider-specific parameters and requirements.

