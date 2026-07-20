# noCRM.io: List Lead Action Histories

Retrieves lead action histories from noCRM.io.

```
GET https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-lead-action-histories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-lead-action-histories?connectionId=$CONNECTION_ID&limit=25&offset=0&leadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "leadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-lead-action-histories?${params}`, {
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
| `leadId` | string | yes | Lead ID. |
| `from` | date | no | Start date for the history range. |
| `to` | date | no | End date for the history range. |
| `actionType` | string | no | Filter by action type. |
| `actionValue` | string | no | Filter by action value. |
| `userIds` | list<string> | no | Comma-separated user IDs or emails. Accepts multiple values in one string, delimited by `,`. |
| `direction` | string | no | Sort direction for returned history. Default: `asc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionItem": {
        "email": "ava@example.com",
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen",
        "name": "Ava Chen",
        "position": 1,
        "type": "string"
      },
      "actionType": "string",
      "createdAt": "string",
      "id": 1,
      "leadId": 1,
      "user": {
        "email": "ava@example.com",
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen",
        "mobilePhone": {},
        "phone": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionItem` | object |  |
| `actionItem.email` | string |  |
| `actionItem.firstname` | string |  |
| `actionItem.id` | number |  |
| `actionItem.lastname` | string |  |
| `actionItem.name` | string |  |
| `actionItem.position` | number |  |
| `actionItem.type` | string |  |
| `actionType` | string |  |
| `createdAt` | string |  |
| `id` | number |  |
| `leadId` | number |  |
| `user` | object |  |
| `user.email` | string |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |
| `user.mobilePhone` | object |  |
| `user.phone` | object |  |

## Native endpoint

Through the native noCRM.io API, this operation is `GET /leads/:lead_id/action_histories` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-lead-action-histories.md) for the provider-specific parameters and requirements.

