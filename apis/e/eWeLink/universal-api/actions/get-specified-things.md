# eWeLink: Get Specified Things

Retrieves specified things from eWeLink.

```
GET https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-specified-things
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-specified-things?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-specified-things?${params}`, {
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
      "thingList": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `thingList[].index` | number |  |
| `thingList[].itemData.apikey` | string |  |
| `thingList[].itemData.deviceid` | string |  |
| `thingList[].itemData.family.familyid` | string |  |
| `thingList[].itemData.family.roomid` | string |  |
| `thingList[].itemData.name` | string |  |
| `thingList[].itemData.params` | object |  |
| `thingList[].itemType` | number |  |

## Native endpoint

Through the native eWeLink API, this operation is `POST /v2/device/thing` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-specified-things.md) for the provider-specific parameters and requirements.

