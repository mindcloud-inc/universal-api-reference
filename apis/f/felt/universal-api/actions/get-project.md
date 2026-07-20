# Felt: Get Project

Retrieves a project from Felt.

```
GET https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-project?${params}`, {
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
| `projectId` | string | yes | Project ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "maps": [
        {}
      ],
      "max_inherited_permission": "string",
      "name": "Ava Chen",
      "type": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Felt project ID. |
| `maps` | array<object> | Maps contained in the project. |
| `max_inherited_permission` | string | Maximum inherited permission. |
| `name` | string | Project name. |
| `type` | string | Returned resource type. |
| `visibility` | string | Project visibility. |

## Native endpoint

Through the native Felt API, this operation is `GET /projects/:projectId` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

