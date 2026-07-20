# Watbot: Delete Contact Variable

Deletes a contact variable from Watbot.

```
DELETE https://connect.mindcloud.co/v1/universal/watbot/latest/actions/delete-contact-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/delete-contact-variable?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watbot/latest/actions/delete-contact-variable?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | no | ID переменной. Обязательно, когда name не передан. |
| `name` | string | no | Имя переменной. Обязательно, когда id не передан. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Watbot API returns.

## Native endpoint

Through the native Watbot API, this operation is `POST /deleteContactVariable` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-variable.md) for the provider-specific parameters and requirements.

