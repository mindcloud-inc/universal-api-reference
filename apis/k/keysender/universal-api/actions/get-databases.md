# Keysender: Get Databases

Retrieves databases from Keysender.

```
GET https://connect.mindcloud.co/v1/universal/keysender/latest/actions/get-databases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keysender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/get-databases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keysender/latest/actions/get-databases?${params}`, {
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
      "available": 1,
      "id": 1,
      "name": "Ava Chen",
      "toSend": 1,
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | number | Available codes in the database. |
| `id` | number | Database identifier. |
| `name` | string | Database name. |
| `toSend` | number | Codes still pending to send. |
| `type` | number | Database type. |

## Native endpoint

Through the native Keysender API, this operation is `GET /databases` (base URL `https://panel.keysender.co.uk/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-databases.md) for the provider-specific parameters and requirements.

