# BotHunter: Set Community Variable

Updates a BotHunter community variable value.

```
PUT https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/set-community-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotHunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/set-community-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "varId": "607d97c6a01c6a25972ed95e",
  "value": "new value"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/set-community-variable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "varId": "607d97c6a01c6a25972ed95e",
    "value": "new value"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `varId` | string | yes | ID of the BotHunter community variable to set. Example: `607d97c6a01c6a25972ed95e`. |
| `value` | string | yes | New value for the community variable. Example: `new value`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true,
      "value": "string",
      "varId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message, when returned. |
| `success` | boolean | Whether BotHunter accepted the set-community-variable request. |
| `value` | string | Value submitted for the community variable. |
| `varId` | string | BotHunter community variable ID used in the request. |

## Native endpoint

Through the native BotHunter API, this operation is `POST /globalvars/set` (base URL `https://smm.targethunter.ru/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-community-variable.md) for the provider-specific parameters and requirements.

