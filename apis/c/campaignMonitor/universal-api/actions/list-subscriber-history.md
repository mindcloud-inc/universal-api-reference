# Campaign Monitor: List Subscriber History

Retrieves history for a Campaign Monitor subscriber by email address.

```
GET https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-subscriber-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-subscriber-history?connectionId=$CONNECTION_ID&listId=string&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string",
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-subscriber-history?${params}`, {
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
| `listId` | string | yes | Campaign Monitor list identifier. |
| `email` | string | yes | Subscriber email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<object> | Subscriber interaction events for the history item. |
| `id` | string | Campaign or workflow identifier in the subscriber history. |
| `name` | string | Campaign or workflow name. |
| `type` | string | History item type, such as Campaign. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `GET /subscribers/:listId/history.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriber-history.md) for the provider-specific parameters and requirements.

