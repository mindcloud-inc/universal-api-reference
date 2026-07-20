# eWeLink: Share Devices

Creates a device sharing entry in eWeLink.

```
POST https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/share-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/share-devices" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/share-devices', {
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
      "updatedThingList": [
        {
          "index": 1,
          "itemData": {
            "apikey": "string",
            "deviceid": "string",
            "name": "Ava Chen",
            "shareTo": {}
          },
          "itemType": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updatedThingList[].index` | number |  |
| `updatedThingList[].itemData.apikey` | string |  |
| `updatedThingList[].itemData.deviceid` | string |  |
| `updatedThingList[].itemData.name` | string |  |
| `updatedThingList[].itemData.shareTo` | object |  |
| `updatedThingList[].itemType` | number |  |

## Native endpoint

Through the native eWeLink API, this operation is `POST /v2/device/share` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/share-devices.md) for the provider-specific parameters and requirements.

