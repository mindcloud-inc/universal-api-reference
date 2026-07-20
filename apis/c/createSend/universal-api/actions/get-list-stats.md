# CreateSend: Get List Stats

Retrieves list stats from CreateSend.

```
GET https://connect.mindcloud.co/v1/universal/createSend/latest/actions/get-list-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CreateSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/createSend/latest/actions/get-list-stats?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/createSend/latest/actions/get-list-stats?${params}`, {
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
| `listId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "TotalActiveSubscribers": 1,
      "Unsubscribes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `TotalActiveSubscribers` | number | Count of active subscribers. |
| `Unsubscribes` | number | Count of unsubscribes. |

## Native endpoint

Through the native CreateSend API, this operation is `GET /lists/:listId/stats.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-stats.md) for the provider-specific parameters and requirements.

