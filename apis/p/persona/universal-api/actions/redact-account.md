# Persona: Redact Account



```
DELETE https://connect.mindcloud.co/v1/universal/persona/latest/actions/redact-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Persona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/persona/latest/actions/redact-account?connectionId=$CONNECTION_ID&accountId=act_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "act_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/persona/latest/actions/redact-account?${params}`, {
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
| `accountId` | string | yes | Account ID Example: `act_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `id` | string |  |
| `relationships` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Persona API, this operation is `DELETE /accounts/[:account-id]` (base URL `https://api.withpersona.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/redact-account.md) for the provider-specific parameters and requirements.

