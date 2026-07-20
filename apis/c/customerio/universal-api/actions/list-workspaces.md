# Customer.io: List Workspaces

Retrieves workspaces from Customer.io.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-workspaces?${params}`, {
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
      "billableMessagesSent": 1,
      "id": 1,
      "messagesSent": 1,
      "name": "Ava Chen",
      "objects": 1,
      "objectTypes": 1,
      "people": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billableMessagesSent` | number | The number of billable messages sent in the current billing period. |
| `id` | number | The id of the workspace. |
| `messagesSent` | number | The number of messages sent in the current billing period. |
| `name` | string | The name of the workspace. |
| `objects` | number | The number of objects in the workspace. |
| `objectTypes` | number | The number of object types in the workspace. |
| `people` | number | The number of people in the workspace. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/workspaces` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

