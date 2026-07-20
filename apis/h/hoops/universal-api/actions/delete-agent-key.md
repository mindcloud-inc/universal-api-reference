# Hoops: Delete Agent Key



```
DELETE https://connect.mindcloud.co/v1/universal/hoops/latest/actions/delete-agent-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hoops `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hoops/latest/actions/delete-agent-key?connectionId=$CONNECTION_ID&nameOrID=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nameOrID": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoops/latest/actions/delete-agent-key?${params}`, {
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
| `nameOrID` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `id` | string |  |

## Native endpoint

Through the native Hoops API, this operation is `DELETE /agents/{nameOrID}` (base URL `https://use.hoop.dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-agent-key.md) for the provider-specific parameters and requirements.

