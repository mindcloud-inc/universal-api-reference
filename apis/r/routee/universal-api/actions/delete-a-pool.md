# Routee: Delete a Pool

Deletes an existing pool from Routee.

```
DELETE https://connect.mindcloud.co/v1/universal/routee/latest/actions/delete-a-pool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/routee/latest/actions/delete-a-pool?connectionId=$CONNECTION_ID&poolId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "poolId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/delete-a-pool?${params}`, {
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
| `poolId` | string | yes | The tracking id of the pool. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedAt": "string",
      "poolId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedAt` | string |  |
| `poolId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `DELETE /pools/my/:poolId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-pool.md) for the provider-specific parameters and requirements.

