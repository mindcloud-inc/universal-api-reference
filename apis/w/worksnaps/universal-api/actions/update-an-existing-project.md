# Worksnaps: Update an existing project

Updates an existing project in Worksnaps.

```
PUT https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/update-an-existing-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/update-an-existing-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "124838",
  "body": "<project><name>MindCloud Validator Project</name><description>Validator fixture project for Worksnaps app build.</description></project>"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/update-an-existing-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "124838",
    "body": "<project><name>MindCloud Validator Project</name><description>Validator fixture project for Worksnaps app build.</description></project>"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | yes | ID of the target project that need to be updated Default: `124838`. |
| `body` | string | yes | Raw XML request body for this Worksnaps endpoint. Default: `<project><name>MindCloud Validator Project</name><description>Validator fixture project for Worksnaps app build.</description></project>`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | the description of the project |
| `id` | number | the ID of the project |
| `name` | string | the name of the project |

## Native endpoint

Through the native Worksnaps API, this operation is `PUT /projects/{project_id}.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-an-existing-project.md) for the provider-specific parameters and requirements.

