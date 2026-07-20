# eWeLink: Get Homes And Rooms

Retrieves homes and rooms from eWeLink.

```
GET https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-homes-and-rooms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-homes-and-rooms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-homes-and-rooms?${params}`, {
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
      "currentFamilyId": "string",
      "familyList": [
        {
          "apikey": "string",
          "id": "string",
          "index": 1,
          "name": "Ava Chen",
          "roomList": [
            {
              "id": "string",
              "index": 1,
              "name": "Ava Chen"
            }
          ]
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
| `currentFamilyId` | string |  |
| `familyList[].apikey` | string |  |
| `familyList[].id` | string |  |
| `familyList[].index` | number |  |
| `familyList[].name` | string |  |
| `familyList[].roomList[].id` | string |  |
| `familyList[].roomList[].index` | number |  |
| `familyList[].roomList[].name` | string |  |

## Native endpoint

Through the native eWeLink API, this operation is `GET /v2/family` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-homes-and-rooms.md) for the provider-specific parameters and requirements.

