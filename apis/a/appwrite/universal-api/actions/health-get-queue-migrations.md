# Appwrite: Get migrations queue

Retrieves Appwrite migrations queue metrics.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/health-get-queue-migrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/health-get-queue-migrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/health-get-queue-migrations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threshold` | number | no | Queue size threshold. When hit (equal or higher), endpoint returns server error. Default value is 5000. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `size` | number | Amount of actions in the queue. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /health/queue/migrations` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/health-get-queue-migrations.md) for the provider-specific parameters and requirements.

