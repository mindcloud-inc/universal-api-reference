# BotHunter: Clear Community Variable

Deletes the value of a BotHunter community variable.

```
DELETE https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/clear-community-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotHunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/clear-community-variable?connectionId=$CONNECTION_ID&varId=607d97c6a01c6a25972ed95e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "varId": "607d97c6a01c6a25972ed95e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/clear-community-variable?${params}`, {
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
| `varId` | string | yes | ID of the BotHunter community variable to clear. Example: `607d97c6a01c6a25972ed95e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true,
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
| `success` | boolean | Whether BotHunter accepted the clear-community-variable request. |
| `varId` | string | BotHunter community variable ID used in the request. |

## Native endpoint

Through the native BotHunter API, this operation is `POST /globalvars/clear` (base URL `https://smm.targethunter.ru/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-community-variable.md) for the provider-specific parameters and requirements.

