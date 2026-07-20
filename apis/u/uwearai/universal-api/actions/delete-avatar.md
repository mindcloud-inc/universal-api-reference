# Uwear.ai: Delete Avatar

Deletes an existing avatar from Uwear.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/delete-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uwear.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/delete-avatar?connectionId=$CONNECTION_ID&avatar_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "avatar_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/delete-avatar?${params}`, {
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
| `avatar_id` | number | yes | Avatar ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detail": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detail` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Uwear.ai API, this operation is `DELETE /api/v1/avatar/:avatar_id` (base URL `https://api.uwear.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-avatar.md) for the provider-specific parameters and requirements.

