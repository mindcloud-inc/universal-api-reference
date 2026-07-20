# AssignX: Get Conversation Detail

Retrieves detailed conversation data from AssignX.

```
GET https://connect.mindcloud.co/v1/universal/assignX/latest/actions/get-conversation-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssignX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assignX/latest/actions/get-conversation-detail?connectionId=$CONNECTION_ID&id=string&cid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "cid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assignX/latest/actions/get-conversation-detail?${params}`, {
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
| `id` | string | yes | The AssignX agent identifier. |
| `cid` | string | yes | The AssignX conversation identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalPages` | number |  |

## Native endpoint

Through the native AssignX API, this operation is `GET agents/:id/conversations/:cid` (base URL `https://api.agentx.so/api/v1/access/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-detail.md) for the provider-specific parameters and requirements.

