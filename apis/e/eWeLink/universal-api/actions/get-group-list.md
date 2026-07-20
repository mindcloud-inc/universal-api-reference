# eWeLink: Get Group List

Retrieves groups from eWeLink.

```
GET https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-group-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-group-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-group-list?${params}`, {
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
      "groupList": [
        {
          "index": 1,
          "itemData": {
            "family": {
              "familyid": "string",
              "index": 1,
              "roomid": "string"
            },
            "id": "string",
            "mainDeviceId": "string",
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
| `groupList[].index` | number |  |
| `groupList[].itemData.family.familyid` | string |  |
| `groupList[].itemData.family.index` | number |  |
| `groupList[].itemData.family.roomid` | string |  |
| `groupList[].itemData.id` | string |  |
| `groupList[].itemData.mainDeviceId` | string |  |
| `groupList[].itemData.name` | string |  |
| `groupList[].itemData.params` | object |  |
| `groupList[].itemType` | number |  |

## Native endpoint

Through the native eWeLink API, this operation is `GET /v2/device/group` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group-list.md) for the provider-specific parameters and requirements.

