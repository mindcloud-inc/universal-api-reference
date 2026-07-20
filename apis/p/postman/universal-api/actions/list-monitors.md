# Postman: List Monitors

Retrieves all available monitors from Postman.

```
GET https://connect.mindcloud.co/v1/universal/postman/latest/actions/list-monitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postman/latest/actions/list-monitors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postman/latest/actions/list-monitors?${params}`, {
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
      "monitors": [
        {
          "active": true,
          "collectionUid": "string",
          "environmentUid": "string",
          "id": "string",
          "name": "Ava Chen",
          "uid": "string"
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
| `monitors[].active` | boolean |  |
| `monitors[].collectionUid` | string |  |
| `monitors[].environmentUid` | string |  |
| `monitors[].id` | string |  |
| `monitors[].name` | string |  |
| `monitors[].uid` | string |  |

## Native endpoint

Through the native Postman API, this operation is `GET /monitors` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-monitors.md) for the provider-specific parameters and requirements.

