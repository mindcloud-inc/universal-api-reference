# eWeLink: Update Group Device List

Updates a group device list in eWeLink.

```
PUT https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/update-group-device-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/update-group-device-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/update-group-device-list', {
  method: 'PUT',
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
            "deviceid": "string",
            "name": "Ava Chen",
            "params": {}
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
| `updatedThingList[].itemData.deviceid` | string |  |
| `updatedThingList[].itemData.name` | string |  |
| `updatedThingList[].itemData.params` | object |  |
| `updatedThingList[].itemType` | number |  |

## Native endpoint

Through the native eWeLink API, this operation is `POST /v2/device/group/update` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group-device-list.md) for the provider-specific parameters and requirements.

