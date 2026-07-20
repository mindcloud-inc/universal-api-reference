# Atlas AI Revenue Engine: Delete Call Record



```
DELETE https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/delete-call-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlas AI Revenue Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/delete-call-record?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/delete-call-record?${params}`, {
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
| `id` | string | yes | The call record ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Atlas AI Revenue Engine API returns.

## Native endpoint

Through the native Atlas AI Revenue Engine API, this operation is `DELETE /call/:id` (base URL `https://api.youratlas.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-call-record.md) for the provider-specific parameters and requirements.

