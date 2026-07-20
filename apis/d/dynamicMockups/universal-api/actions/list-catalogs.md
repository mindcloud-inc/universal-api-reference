# Dynamic Mockups: List Catalogs

Retrieves your catalogs from Dynamic Mockups.

```
GET https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/list-catalogs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynamic Mockups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/list-catalogs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/list-catalogs?${params}`, {
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
      "data": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdAtTimestamp": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "type": "string",
          "uuid": "string"
        }
      ],
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].createdAt` | date |  |
| `data[].createdAtTimestamp` | date |  |
| `data[].name` | string |  |
| `data[].type` | string |  |
| `data[].uuid` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Dynamic Mockups API, this operation is `GET api/v1/catalogs` (base URL `https://app.dynamicmockups.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-catalogs.md) for the provider-specific parameters and requirements.

