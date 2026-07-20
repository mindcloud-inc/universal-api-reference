# Nutshell: Create Lead

Creates a new lead in Nutshell.

```
POST https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutshell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leads[].description` | string | no | Description for the lead. |
| `leads[].manualValue` | string | no | Manual value to assign to the lead. |
| `leads[].dueTime.timestamp` | date | no | Due time for the lead. |
| `leads[].links.accounts[]` | array<string> | no | Company IDs to link to the lead. Accepts multiple values as an array. |
| `leads[].links.contacts[]` | array<string> | no | Contact IDs to link to the lead. Accepts multiple values as an array. |
| `leads[].links.owner` | string | no | User ID to assign as the lead owner. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anticipatedClosedTime": {},
      "avatarUrl": "https://example.com",
      "closedTime": {},
      "confidence": 1,
      "createdTime": {
        "absoluteLocalizedString": "string",
        "timestamp": "2026-05-07T12:00:00.000Z",
        "value": "2026-05-07T12:00:00.000Z"
      },
      "deletedTime": {},
      "description": "string",
      "dueTime": {},
      "href": "string",
      "htmlUrl": "https://example.com",
      "htmlUrlPath": "https://example.com",
      "id": "string",
      "initials": {},
      "isCurrentUserWatching": true,
      "isOverdue": true,
      "lastContactedTime": {},
      "links": {
        "accounts": [
          "https://example.com"
        ],
        "contacts": [
          "https://example.com"
        ],
        "creator": "https://example.com",
        "market": "https://example.com",
        "outcome": {},
        "owner": {},
        "stage": {},
        "stageset": {},
        "territory": {}
      },
      "name": "Ava Chen",
      "number": "string",
      "overdueTime": {},
      "ownerType": {},
      "pieState": "string",
      "priority": 1,
      "status": "string",
      "type": "string",
      "value": {
        "amount": 1,
        "currency": "string",
        "formatted": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anticipatedClosedTime` | object |  |
| `avatarUrl` | string |  |
| `closedTime` | object |  |
| `confidence` | number |  |
| `createdTime.absoluteLocalizedString` | string |  |
| `createdTime.timestamp` | date |  |
| `createdTime.value` | date |  |
| `deletedTime` | object |  |
| `description` | string |  |
| `dueTime` | object |  |
| `href` | string |  |
| `htmlUrl` | string |  |
| `htmlUrlPath` | string |  |
| `id` | string |  |
| `initials` | object |  |
| `isCurrentUserWatching` | boolean |  |
| `isOverdue` | boolean |  |
| `lastContactedTime` | object |  |
| `links.accounts[]` | string |  |
| `links.contacts[]` | string |  |
| `links.creator` | string |  |
| `links.market` | string |  |
| `links.outcome` | object |  |
| `links.owner` | object |  |
| `links.stage` | object |  |
| `links.stageset` | object |  |
| `links.territory` | object |  |
| `name` | string |  |
| `number` | string |  |
| `overdueTime` | object |  |
| `ownerType` | object |  |
| `pieState` | string |  |
| `priority` | number |  |
| `status` | string |  |
| `type` | string |  |
| `value.amount` | number |  |
| `value.currency` | string |  |
| `value.formatted` | string |  |

## Native endpoint

Through the native Nutshell API, this operation is `POST /leads` (base URL `https://app.nutshell.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

