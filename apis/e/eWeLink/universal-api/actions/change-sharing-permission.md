# eWeLink: Change Sharing Permission

Updates a sharing permission in eWeLink.

```
PUT https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/change-sharing-permission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/change-sharing-permission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/change-sharing-permission', {
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
      "updatedThing": [
        {
          "index": 1,
          "itemData": {
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
| `updatedThing[].index` | number |  |
| `updatedThing[].itemData.deviceid` | string |  |
| `updatedThing[].itemData.name` | string |  |
| `updatedThing[].itemData.shareTo` | object |  |
| `updatedThing[].itemType` | number |  |

## Native endpoint

Through the native eWeLink API, this operation is `POST /v2/device/share/permit` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-sharing-permission.md) for the provider-specific parameters and requirements.

