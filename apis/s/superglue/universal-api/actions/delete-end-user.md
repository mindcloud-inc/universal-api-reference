# Superglue: Delete End User



```
DELETE https://connect.mindcloud.co/v1/universal/superglue/latest/actions/delete-end-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superglue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/delete-end-user?connectionId=$CONNECTION_ID&endUserId=550e8400-e29b-41d4-a716-446655440000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endUserId": "550e8400-e29b-41d4-a716-446655440000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superglue/latest/actions/delete-end-user?${params}`, {
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
| `endUserId` | string | yes | Internal Superglue end-user ID. Example: `550e8400-e29b-41d4-a716-446655440000`. |

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
| `success` | boolean | Whether the end user was deleted. |

## Native endpoint

Through the native Superglue API, this operation is `DELETE /end-users/:endUserId` (base URL `https://api.superglue.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-end-user.md) for the provider-specific parameters and requirements.

