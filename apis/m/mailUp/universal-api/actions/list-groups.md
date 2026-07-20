# MailUp: List Groups

Retrieves groups from a MailUp list.

```
GET https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-groups?connectionId=$CONNECTION_ID&idList=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idList": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-groups?${params}`, {
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
      "count": 1,
      "deletable": true,
      "idGroup": 1,
      "idList": 1,
      "name": "Ava Chen",
      "notes": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `deletable` | boolean |  |
| `idGroup` | number |  |
| `idList` | number |  |
| `name` | string |  |
| `notes` | string |  |

## Native endpoint

Through the native MailUp API, this operation is `GET Console/List/:id_List/Groups` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

