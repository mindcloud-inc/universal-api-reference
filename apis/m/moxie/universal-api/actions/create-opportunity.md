# Moxie: Create Opportunity

Creates a new opportunity in Moxie.

```
POST https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-opportunity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Opportunity name. |
| `description` | string | no | Opportunity description. |
| `clientName` | string | no | Existing client name for the opportunity. |
| `stageName` | string | no | Pipeline stage name. |
| `value` | number | no | Opportunity value. |
| `estCloseDate` | string | no | Estimated close date in YYYY-MM-DD format. Example: `2026-03-21`. |
| `leadInfo` | object | no | Lead info object for a new opportunity. |
| `toDos` | list<object> | no | List of opportunity to-do items. |
| `customValues` | object | no | Custom values object for the opportunity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "archive": true,
      "client": {},
      "clientId": "string",
      "comments": [
        {}
      ],
      "customValues": [
        {}
      ],
      "description": "string",
      "estCloseDate": "2026-05-07T12:00:00.000Z",
      "files": [
        {}
      ],
      "formData": {},
      "history": [
        {}
      ],
      "id": "string",
      "initialWorkflow": true,
      "name": "Ava Chen",
      "periods": 1,
      "sampleData": true,
      "statusId": "string",
      "statusLabel": "string",
      "timePeriod": "string",
      "toDos": [
        {}
      ],
      "value": 1,
      "workflow": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `archive` | boolean |  |
| `client` | object |  |
| `clientId` | string |  |
| `comments` | array<object> |  |
| `customValues` | array<object> |  |
| `description` | string |  |
| `estCloseDate` | date |  |
| `files` | array<object> |  |
| `formData` | object |  |
| `history` | array<object> |  |
| `id` | string |  |
| `initialWorkflow` | boolean |  |
| `name` | string |  |
| `periods` | number |  |
| `sampleData` | boolean |  |
| `statusId` | string |  |
| `statusLabel` | string |  |
| `timePeriod` | string |  |
| `toDos` | array<object> |  |
| `value` | number |  |
| `workflow` | array<object> |  |

## Native endpoint

Through the native Moxie API, this operation is `POST /action/opportunities/create` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity.md) for the provider-specific parameters and requirements.

