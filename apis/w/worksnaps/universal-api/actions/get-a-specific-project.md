# Worksnaps: Get a specific project

Retrieves a specific project from Worksnaps.

```
GET https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-a-specific-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-a-specific-project?connectionId=$CONNECTION_ID&project_id=124838" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "124838"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-a-specific-project?${params}`, {
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
| `project_id` | number | yes | ID of the target project that needs to be fetched Default: `124838`. |

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

Through the native Worksnaps API, this operation is `GET /projects/{project_id}.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-specific-project.md) for the provider-specific parameters and requirements.

