# RotaCloud: Delete Shifts Batch



```
DELETE https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/delete-shifts-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/delete-shifts-batch?connectionId=$CONNECTION_ID&ids%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/delete-shifts-batch?${params}`, {
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
| `ids[]` | array<number> | yes | Shift IDs to delete in batch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "error": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `error` | string |  |
| `id` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `DELETE /v1/shifts` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-shifts-batch.md) for the provider-specific parameters and requirements.

