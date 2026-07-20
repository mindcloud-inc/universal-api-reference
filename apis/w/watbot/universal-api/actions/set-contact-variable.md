# Watbot: Set Contact Variable

Sets a contact variable in Watbot.

```
PUT https://connect.mindcloud.co/v1/universal/watbot/latest/actions/set-contact-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/set-contact-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": 1,
  "name": "Ava Chen",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/watbot/latest/actions/set-contact-variable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": 1,
    "name": "Ava Chen",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | yes | ID контакта. |
| `name` | string | yes | Имя переменной. |
| `value` | string | yes | Значение переменной. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deletable` | number | no | 0 — не удалять после заявки, 1 — удалять после заявки. Default: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Watbot API returns.

## Native endpoint

Through the native Watbot API, this operation is `POST /setContactVariable` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-contact-variable.md) for the provider-specific parameters and requirements.

