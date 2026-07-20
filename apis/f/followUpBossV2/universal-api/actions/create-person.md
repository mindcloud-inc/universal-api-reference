# Follow Up Boss: Create Person

Creates a new person in Follow Up Boss.

```
POST https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-person', {
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
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `source` | string | no |  |
| `sourceUrl` | string | no |  |
| `stage` | string | no |  |
| `assignedTo` | string | no |  |
| `contacted` | boolean | no |  |
| `createdAt` | date | no |  |
| `emails[].value` | string | no |  |
| `emails[].type` | string | no |  |
| `emails[].isPrimary` | boolean | no |  |
| `phones[].value` | string | no |  |
| `phones[].type` | string | no |  |
| `phones[].isPrimary` | boolean | no |  |
| `addresses[].type` | string | no |  |
| `addresses[].street` | string | no |  |
| `addresses[].city` | string | no |  |
| `addresses[].state` | string | no |  |
| `addresses[].code` | string | no |  |
| `addresses[].country` | string | no |  |
| `tags[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "assignedLenderId": 1,
      "assignedLenderName": "Ava Chen",
      "assignedPondId": 1,
      "assignedTo": "string",
      "assignedUserId": 1,
      "claimed": true,
      "collaborators": [
        {}
      ],
      "contacted": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "createdVia": "string",
      "delayed": true,
      "emails": [
        {}
      ],
      "firstName": "Ava",
      "id": 1,
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "name": "Ava Chen",
      "phones": [
        {}
      ],
      "picture": {},
      "pondMembers": [
        {}
      ],
      "source": "string",
      "sourceId": 1,
      "sourceUrl": "https://example.com",
      "stage": "string",
      "stageId": 1,
      "tags": [
        "string"
      ],
      "teamLeaders": [
        {}
      ],
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "websiteVisits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `assignedLenderId` | number |  |
| `assignedLenderName` | string |  |
| `assignedPondId` | number |  |
| `assignedTo` | string |  |
| `assignedUserId` | number |  |
| `claimed` | boolean |  |
| `collaborators` | array<object> |  |
| `contacted` | number |  |
| `created` | date |  |
| `createdVia` | string |  |
| `delayed` | boolean |  |
| `emails` | array<object> |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastActivity` | date |  |
| `lastName` | string |  |
| `name` | string |  |
| `phones` | array<object> |  |
| `picture` | object |  |
| `pondMembers` | array<object> |  |
| `source` | string |  |
| `sourceId` | number |  |
| `sourceUrl` | string |  |
| `stage` | string |  |
| `stageId` | number |  |
| `tags` | array<string> |  |
| `teamLeaders` | array<object> |  |
| `type` | string |  |
| `updated` | date |  |
| `websiteVisits` | number |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `POST people` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.

