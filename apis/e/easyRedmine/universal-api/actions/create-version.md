# Easy Redmine: Create Version

Creates a new version in an Easy Redmine project.

```
POST https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/create-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Redmine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/create-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "version": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/create-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "version": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | ID of the project to create the version in. |
| `version` | object | yes | Version payload to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "effectiveDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "project": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `dueDate` | date |  |
| `effectiveDate` | date |  |
| `id` | number |  |
| `name` | string |  |
| `project` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Easy Redmine API, this operation is `POST /projects/:projectId/versions.json` (base URL `https://3f73561b8b.bigus-e5.easy8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-version.md) for the provider-specific parameters and requirements.

