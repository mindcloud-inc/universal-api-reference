# Loopy Loyalty: List Locations



```
GET https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-locations?${params}`, {
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
        "address": "string",
        "id": "string",
        "lat": 1,
        "lon": 1,
        "name": "Ava Chen",
        "object": "string",
        "showAddressOnCard": true,
        "uid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value.address` | string | Human readable address. |
| `value.id` | string | Location ID. |
| `value.lat` | number | Latitude. |
| `value.lon` | number | Longitude. |
| `value.name` | string | Location name. |
| `value.object` | string | Resource type marker. |
| `value.showAddressOnCard` | boolean | Whether the address is shown on the card. |
| `value.uid` | string | Owner user ID. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `GET /locations` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

