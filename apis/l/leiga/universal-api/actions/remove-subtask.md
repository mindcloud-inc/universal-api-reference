# Leiga: Remove Subtask

Deletes an existing subtask from Leiga.

```
DELETE https://connect.mindcloud.co/v1/universal/leiga/latest/actions/remove-subtask
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/remove-subtask?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/remove-subtask?${params}`, {
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
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the subtask removal succeeded. |

## Native endpoint

Through the native Leiga API, this operation is `DELETE /issue/remove-subtask` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-subtask.md) for the provider-specific parameters and requirements.

