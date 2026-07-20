# eWeLink: HomePage

Retrieves homepage device data from eWeLink.

```
GET https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/homepage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/homepage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/homepage?${params}`, {
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
      "familyInfo": {
        "currentFamilyId": "string",
        "familyList": [
          {
            "id": "string",
            "name": "Ava Chen"
          }
        ]
      },
      "messageInfo": {
        "messageList": [
          {
            "msgid": "string"
          }
        ]
      },
      "thingInfo": {
        "thingList": [
          {
            "itemData": {
              "deviceid": "string"
            },
            "itemType": 1
          }
        ],
        "total": 1
      },
      "userInfo": {
        "user": {
          "apikey": "string",
          "email": "ava@example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `familyInfo.currentFamilyId` | string |  |
| `familyInfo.familyList[].id` | string |  |
| `familyInfo.familyList[].name` | string |  |
| `messageInfo.messageList[].msgid` | string |  |
| `thingInfo.thingList[].itemData.deviceid` | string |  |
| `thingInfo.thingList[].itemType` | number |  |
| `thingInfo.total` | number |  |
| `userInfo.user.apikey` | string |  |
| `userInfo.user.email` | string |  |

## Native endpoint

Through the native eWeLink API, this operation is `POST /v2/homepage` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/homepage.md) for the provider-specific parameters and requirements.

