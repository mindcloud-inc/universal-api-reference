# eWeLink: Cancel Sharing

Deletes a sharing permission from eWeLink.

```
DELETE https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/cancel-sharing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/cancel-sharing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/cancel-sharing?${params}`, {
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

Through the native eWeLink API, this operation is `DELETE /v2/device/share` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-sharing.md) for the provider-specific parameters and requirements.

