# SalesapCRM: Update Diary Task

Updates a diary task in SalesapCRM.

```
PUT https://connect.mindcloud.co/v1/universal/salesapCRM/latest/actions/update-diary-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesapCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesapCRM/latest/actions/update-diary-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesapCRM/latest/actions/update-diary-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | SalesapCRM diary task record ID from the path. |
| `data` | object | yes | JSON:API data object for updating a diary task, including type, attributes, and optional relationships. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "links": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `id` | string |  |
| `links` | object |  |
| `relationships` | object |  |
| `type` | string |  |

## Native endpoint

Through the native SalesapCRM API, this operation is `PATCH /diary-tasks/{id}` (base URL `https://app.salesap.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-diary-task.md) for the provider-specific parameters and requirements.

