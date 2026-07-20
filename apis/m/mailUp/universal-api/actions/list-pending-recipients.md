# MailUp: List Pending Recipients

Retrieves pending recipients from a MailUp list.

```
GET https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-pending-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-pending-recipients?connectionId=$CONNECTION_ID&idList=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idList": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-pending-recipients?${params}`, {
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
| `idList` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "fields": [
        {}
      ],
      "idRecipient": 1,
      "mobileNumber": "string",
      "mobilePrefix": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `fields` | array<object> |  |
| `idRecipient` | number |  |
| `mobileNumber` | string |  |
| `mobilePrefix` | string |  |
| `name` | string |  |

## Native endpoint

Through the native MailUp API, this operation is `GET Console/List/:id_List/Recipients/Pending` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pending-recipients.md) for the provider-specific parameters and requirements.

