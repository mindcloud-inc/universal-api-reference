# Zoominfo: Get Buying Groups

Retrieves buying groups from ZoomInfo.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-buying-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-buying-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-buying-groups?${params}`, {
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
      "accessLevel": "string",
      "id": 1,
      "isDefault": true,
      "name": "Ava Chen",
      "personas": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | string |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `personas` | array<object> |  |

## Native endpoint

Through the native Zoominfo API, this operation is `GET lookup/buyinggroups` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-buying-groups.md) for the provider-specific parameters and requirements.

