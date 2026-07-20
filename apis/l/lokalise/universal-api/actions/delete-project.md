# Lokalise: Delete Project

Deletes an existing project from Lokalise.

```
DELETE https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/delete-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lokalise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/delete-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/delete-project?${params}`, {
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
| `project_id` | string | no | Lokalise project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "project_deleted": true,
      "project_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `project_deleted` | boolean |  |
| `project_id` | string |  |

## Native endpoint

Through the native Lokalise API, this operation is `DELETE /projects/:project_id` (base URL `https://api.lokalise.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project.md) for the provider-specific parameters and requirements.

