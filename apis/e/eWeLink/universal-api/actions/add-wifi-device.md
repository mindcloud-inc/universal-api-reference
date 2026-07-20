# eWeLink: Add WiFi Device

Creates a new Wi-Fi device in eWeLink.

```
POST https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/add-wifi-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/add-wifi-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/add-wifi-device', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "index": 1,
      "itemData": {
        "apikey": "string",
        "deviceid": "string",
        "family": {
          "familyid": "string",
          "roomid": "string"
        },
        "name": "Ava Chen",
        "params": {}
      },
      "itemType": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `index` | number |  |
| `itemData.apikey` | string |  |
| `itemData.deviceid` | string |  |
| `itemData.family.familyid` | string |  |
| `itemData.family.roomid` | string |  |
| `itemData.name` | string |  |
| `itemData.params` | object |  |
| `itemType` | number |  |

## Native endpoint

Through the native eWeLink API, this operation is `POST /v2/device/add` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-wifi-device.md) for the provider-specific parameters and requirements.

