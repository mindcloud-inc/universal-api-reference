# Sempico Solutions SMS: Create Group



```
POST https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/create-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sempico Solutions SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name_group": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name_group": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name_group` | string | yes | Name for the new group. |
| `on_birth` | boolean | no | Whether birthday greetings should be sent for this group. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `time_birth` | string | no | Optional time for birthday greeting messages. |
| `originator_birth` | string | no | Optional sender ID for birthday greeting messages. |
| `text_birth` | string | no | Optional birthday greeting text. Sempico supports replacing #first_name# with the contact name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupDetails": {
        "command": "string",
        "createCount": 1
      },
      "list": {
        "id_group": 1,
        "name_group": "Ava Chen",
        "numbers_count": 1,
        "on_birth": true,
        "originator_birth": "string",
        "text_birth": "string",
        "time_birth": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupDetails.command` | string | Operation performed. |
| `groupDetails.createCount` | number | Number of groups created. |
| `list` | array<object> | Created group records. |
| `list.id_group` | number | Created group ID. |
| `list.name_group` | string | Created group name. |
| `list.numbers_count` | number | Number of phone numbers in the group. |
| `list.on_birth` | boolean | Whether birthday greetings are enabled. |
| `list.originator_birth` | string | Birthday greeting sender ID, when configured. |
| `list.text_birth` | string | Birthday greeting text, when configured. |
| `list.time_birth` | string | Birthday greeting time, when configured. |

## Native endpoint

Through the native Sempico Solutions SMS API, this operation is `POST /group-create` (base URL `https://restapi.sempico.solutions/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group.md) for the provider-specific parameters and requirements.

