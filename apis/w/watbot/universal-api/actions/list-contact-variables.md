# Watbot: List Contact Variables

Retrieves contact variables from Watbot.

```
GET https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-contact-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-contact-variables?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-contact-variables?${params}`, {
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
| `contactId` | number | yes | ID контакта. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletable": true,
      "id": 1,
      "name": "Ava Chen",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletable` | boolean | Удаляется ли переменная после заявки. |
| `id` | number | ID переменной контакта. |
| `name` | string | Имя переменной. |
| `value` | string | Значение переменной. |

## Native endpoint

Through the native Watbot API, this operation is `GET /getContactVariables` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-variables.md) for the provider-specific parameters and requirements.

