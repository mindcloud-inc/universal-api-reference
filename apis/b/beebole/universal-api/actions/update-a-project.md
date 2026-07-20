# Beebole: Update a Project

Updates an existing project in Beebole.

```
PUT https://connect.mindcloud.co/v1/universal/beebole/latest/actions/update-a-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beebole `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/update-a-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project.id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beebole/latest/actions/update-a-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project.id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project.id` | number | yes | The Beebole project ID to update. |
| `project.name` | string | no | Updated project name. |
| `project.startDate` | string | no | Updated project start date in YYYY-MM-DD format. |
| `project.description` | string | no | Updated project description. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beebole API returns.

## Native endpoint

Through the native Beebole API, this operation is `POST` (base URL `https://beebole-apps.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-project.md) for the provider-specific parameters and requirements.

