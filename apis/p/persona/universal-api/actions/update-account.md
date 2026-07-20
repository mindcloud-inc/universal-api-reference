# Persona: Update Account



```
PUT https://connect.mindcloud.co/v1/universal/persona/latest/actions/update-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Persona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/persona/latest/actions/update-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "act_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/persona/latest/actions/update-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "act_123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Account ID Example: `act_123`. |
| `referenceId` | string | no | Reference ID Example: `mindcloud-account-updated`. |

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

Through the native Persona API, this operation is `PATCH /accounts/[:account-id]` (base URL `https://api.withpersona.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account.md) for the provider-specific parameters and requirements.

