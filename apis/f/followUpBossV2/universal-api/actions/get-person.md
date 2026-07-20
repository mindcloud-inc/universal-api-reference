# Follow Up Boss: Get Person

Retrieves a person from Follow Up Boss.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-person?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-person?${params}`, {
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
| `id` | string | yes | The person ID. |

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

Through the native Follow Up Boss API, this operation is `GET people/:id` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

