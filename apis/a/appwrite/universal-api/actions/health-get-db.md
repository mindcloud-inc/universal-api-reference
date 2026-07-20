# Appwrite: Get DB

Retrieves Appwrite database health status.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/health-get-db
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/health-get-db?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/health-get-db?${params}`, {
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
      "name": "Ava Chen",
      "ping": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Name of the service. |
| `ping` | number | Duration in milliseconds how long the health check took. |
| `status` | string | Service status. Possible values are: `pass`, `fail` |

## Native endpoint

Through the native Appwrite API, this operation is `GET /health/db` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/health-get-db.md) for the provider-specific parameters and requirements.

