# ChatDaddy: Delete Account

Enqueues deletion of an account in ChatDaddy.

```
DELETE https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/delete-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/delete-account?connectionId=$CONNECTION_ID&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/delete-account?${params}`, {
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
| `accountId` | string | yes | Account identifier to delete. |

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
| `success` | boolean | Whether the account deletion completed successfully. |

## Native endpoint

Through the native ChatDaddy API, this operation is `DELETE /accounts/{accountId}` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-account.md) for the provider-specific parameters and requirements.

