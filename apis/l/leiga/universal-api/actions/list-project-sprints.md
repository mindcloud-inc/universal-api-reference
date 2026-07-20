# Leiga: List Project Sprints

Retrieves sprints for a project in Leiga.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-project-sprints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-project-sprints?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-project-sprints?${params}`, {
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
| `projectId` | number | yes | Project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": 1,
      "assigneeName": "Ava Chen",
      "completeDate": 1,
      "endDate": 1,
      "estimatePointTotal": 1,
      "goal": "string",
      "id": 1,
      "issueTypeCountMap": {},
      "name": "Ava Chen",
      "startDate": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | number | Sprint owner ID. |
| `assigneeName` | string | Sprint owner name. |
| `completeDate` | number | Completion timestamp. |
| `endDate` | number | End timestamp. |
| `estimatePointTotal` | number | Total estimate points. |
| `goal` | string | Sprint goal. |
| `id` | number | Sprint ID. |
| `issueTypeCountMap` | object | Issue counts by type. |
| `name` | string | Sprint name. |
| `startDate` | number | Start timestamp. |
| `status` | number | Sprint status. |

## Native endpoint

Through the native Leiga API, this operation is `POST /sprint/list-with-count` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-sprints.md) for the provider-specific parameters and requirements.

