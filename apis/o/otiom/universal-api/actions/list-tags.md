# Otiom: List Tags

Retrieves tags from Otiom.

```
GET https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Otiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-tags?${params}`, {
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
      "administrating": true,
      "alarm_status": 1,
      "battery_charge": 1,
      "battery_status": 1,
      "buoy_seen_on": "string",
      "history": [
        "string"
      ],
      "id": 1,
      "last_location": {},
      "last_location_accuracy": 1,
      "last_location_accuracy_growth": "string",
      "last_location_hdop": 1,
      "last_location_name": "Ava Chen",
      "last_location_pdop": 1,
      "last_location_ts": "string",
      "last_message": "string",
      "last_seen_buoy": 1,
      "location_active": true,
      "mac_address": "string",
      "name": "Ava Chen",
      "network_active": true,
      "otiom_tag_model": 1,
      "tag_color": "string",
      "temperature": 1,
      "zone": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrating` | boolean |  |
| `alarm_status` | number |  |
| `battery_charge` | number |  |
| `battery_status` | number |  |
| `buoy_seen_on` | string |  |
| `history` | array |  |
| `id` | number |  |
| `last_location` | object |  |
| `last_location_accuracy` | number |  |
| `last_location_accuracy_growth` | string |  |
| `last_location_hdop` | number |  |
| `last_location_name` | string |  |
| `last_location_pdop` | number |  |
| `last_location_ts` | string |  |
| `last_message` | string |  |
| `last_seen_buoy` | number |  |
| `location_active` | boolean |  |
| `mac_address` | string |  |
| `name` | string |  |
| `network_active` | boolean |  |
| `otiom_tag_model` | number |  |
| `tag_color` | string |  |
| `temperature` | number |  |
| `zone` | number |  |

## Native endpoint

Through the native Otiom API, this operation is `GET /api/tag/` (base URL `https://api.otiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

