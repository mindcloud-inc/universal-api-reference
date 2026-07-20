# KeyVox: List Available Places

Lists available places in your KeyVox account.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-available-places
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-available-places?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-available-places?${params}`, {
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
      "unitAvailableList": [
        {
          "placeId": "string",
          "placeName": "Ava Chen",
          "unitId": "string",
          "unitName": "Ava Chen"
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
| `unitAvailableList[].placeId` | string | 場所ID |
| `unitAvailableList[].placeName` | string | 場所名 |
| `unitAvailableList[].unitId` | string | 部屋ID |
| `unitAvailableList[].unitName` | string | 部屋名 |

## Native endpoint

Through the native KeyVox API, this operation is `POST /place/availableList` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-places.md) for the provider-specific parameters and requirements.

