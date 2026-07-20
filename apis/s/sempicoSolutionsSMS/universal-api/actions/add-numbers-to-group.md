# Sempico Solutions SMS: Add Numbers to Group



```
POST https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/add-numbers-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sempico Solutions SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/add-numbers-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id_group": 1,
  "numbers[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/add-numbers-to-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id_group": 1,
    "numbers[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id_group` | number | yes | Group ID to add numbers to. |
| `numbers[]` | array<object> | yes | Numbers to add to the group. Each item can include number plus optional name, surname, patronymic, date_birth, male, and note_1 through note_10 fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupDetails": {
        "countPhoneAfter": 1,
        "countPhoneBefore": 1,
        "id_group": 1,
        "name_group": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupDetails.countPhoneAfter` | number | Number count after adding. |
| `groupDetails.countPhoneBefore` | number | Number count before adding. |
| `groupDetails.id_group` | number | Group ID. |
| `groupDetails.name_group` | string | Group name. |

## Native endpoint

Through the native Sempico Solutions SMS API, this operation is `POST /group-number-add` (base URL `https://restapi.sempico.solutions/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-numbers-to-group.md) for the provider-specific parameters and requirements.

