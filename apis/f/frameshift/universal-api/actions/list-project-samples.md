# Frameshift: List Project Samples

Retrieves a list of project samples from Frameshift.

```
GET https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-project-samples
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-project-samples?connectionId=$CONNECTION_ID&project_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-project-samples?${params}`, {
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
| `project_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "id": 1,
      "isSampled": true,
      "name": "Ava Chen",
      "subProjectId": 1,
      "uid": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | number |  |
| `isSampled` | boolean |  |
| `name` | string |  |
| `subProjectId` | number |  |
| `uid` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Frameshift API, this operation is `GET /v1/projects/:project_id/samples` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-samples.md) for the provider-specific parameters and requirements.

