# Moco: List Planning Entries



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-planning-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-planning-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-planning-entries?${params}`, {
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
| `customProperties` | object | no |  |
| `dealId` | number | no |  |
| `ids` | string | no |  |
| `period` | string | no |  |
| `projectId` | number | no |  |
| `updatedAfter` | date | no |  |
| `userId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "comment": "string",
      "createdAt": "string",
      "deal": {},
      "endsOn": "string",
      "hoursPerDay": 1,
      "id": 1,
      "project": {
        "color": "string",
        "customerName": "Ava Chen",
        "id": 1,
        "identifier": "string",
        "name": "Ava Chen"
      },
      "readOnly": true,
      "seriesId": {},
      "seriesRepeat": {},
      "startsOn": "string",
      "symbol": {},
      "task": {},
      "tentative": true,
      "title": "string",
      "updatedAt": "string",
      "user": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `comment` | string |  |
| `createdAt` | string |  |
| `deal` | object |  |
| `endsOn` | string |  |
| `hoursPerDay` | number |  |
| `id` | number |  |
| `project` | object |  |
| `project.color` | string |  |
| `project.customerName` | string |  |
| `project.id` | number |  |
| `project.identifier` | string |  |
| `project.name` | string |  |
| `readOnly` | boolean |  |
| `seriesId` | object |  |
| `seriesRepeat` | object |  |
| `startsOn` | string |  |
| `symbol` | object |  |
| `task` | object |  |
| `tentative` | boolean |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `user` | object |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |

## Native endpoint

Through the native Moco API, this operation is `GET /planning_entries` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-planning-entries.md) for the provider-specific parameters and requirements.

