# Nexiopay: Delete card tokens



```
DELETE https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/delete-card-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/delete-card-tokens?connectionId=$CONNECTION_ID&tokens%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tokens[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/delete-card-tokens?${params}`, {
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
| `tokens[]` | array<string> | yes | Array of saved card tokens to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "message": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether token deletion succeeded. |
| `message` | string | Nexio response message. |
| `token` | string | Deleted token. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /pay/v3/deleteToken` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-card-tokens.md) for the provider-specific parameters and requirements.

