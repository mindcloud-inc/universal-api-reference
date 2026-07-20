# SMSEdge: Get List Details

Retrieves details for a list in SMSEdge.

```
GET https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/get-list-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSEdge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/get-list-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/get-list-details?${params}`, {
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
| `id` | string | yes | ID of requested list |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMSEdge API returns.

## Native endpoint

Through the native SMSEdge API, this operation is `GET /lists/info/` (base URL `https://api.smsedge.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-details.md) for the provider-specific parameters and requirements.

