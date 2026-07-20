# eWeLink: Change Device Tags

Updates device tags in eWeLink.

```
PUT https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/change-device-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/change-device-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/change-device-tags', {
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
      "updatedThing": {
        "index": 1,
        "itemData": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updatedThing.index` | number |  |
| `updatedThing.itemData.deviceid` | string |  |
| `updatedThing.itemData.family.familyid` | string |  |
| `updatedThing.itemData.family.roomid` | string |  |
| `updatedThing.itemData.name` | string |  |
| `updatedThing.itemData.params` | object |  |
| `updatedThing.itemType` | number |  |

## Native endpoint

Through the native eWeLink API, this operation is `POST /v2/device/tags` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-device-tags.md) for the provider-specific parameters and requirements.

