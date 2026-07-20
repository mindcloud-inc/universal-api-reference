# LinkedCamp: Cancel Sub-Account



```
DELETE https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/cancel-sub-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedCamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/cancel-sub-account?connectionId=$CONNECTION_ID&email=ava%40example.com&reason=string&description=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com",
  "reason": "string",
  "description": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/cancel-sub-account?${params}`, {
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
| `email` | string | yes | Sub-account email address. |
| `reason` | string | yes | Cancellation reason. |
| `description` | string | yes | Cancellation description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider response message. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native LinkedCamp API, this operation is `POST /users/cancel` (base URL `https://api.linkedcamp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-sub-account.md) for the provider-specific parameters and requirements.

