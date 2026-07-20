# Clockodo: Update Project

Updates a project in your Clockodo account.

```
PUT https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockodo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | boolean | no |  |
| `billableDefault` | boolean | no |  |
| `billedCompletely` | boolean | no |  |
| `billedMoney` | number | no |  |
| `budgetIsHours` | boolean | no |  |
| `budgetIsNotStrict` | boolean | no |  |
| `budgetMoney` | number | no |  |
| `completed` | boolean | no |  |
| `customersId` | string | no |  |
| `deadline` | string | no |  |
| `id` | string | yes |  |
| `name` | string | no |  |
| `note` | string | no |  |
| `number` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "billableDefault": true,
      "billedCompletely": true,
      "billedMoney": 1,
      "budgetIsHours": true,
      "budgetIsNotStrict": true,
      "budgetMoney": 1,
      "completed": true,
      "customersId": "string",
      "deadline": "string",
      "id": "string",
      "name": "Ava Chen",
      "note": "string",
      "number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `billableDefault` | boolean |  |
| `billedCompletely` | boolean |  |
| `billedMoney` | number |  |
| `budgetIsHours` | boolean |  |
| `budgetIsNotStrict` | boolean |  |
| `budgetMoney` | number |  |
| `completed` | boolean |  |
| `customersId` | string |  |
| `deadline` | string |  |
| `id` | string |  |
| `name` | string |  |
| `note` | string |  |
| `number` | string |  |

## Native endpoint

Through the native Clockodo API, this operation is `PUT /projects/:id` (base URL `https://my.clockodo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

