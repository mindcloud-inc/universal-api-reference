# FogBugz: List Projects

Retrieves projects from FogBugz.

```
GET https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FogBugz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-projects?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fWrite` | boolean | no | Set to true to include only projects you can modify. |
| `ixProject` | number | no | Include a specific project even if it is deleted. |
| `fDeleted` | boolean | no | Set to true to include deleted projects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fDeleted": true,
      "fInbox": true,
      "ixPersonOwner": 1,
      "ixProject": 1,
      "ixWorkflow": 1,
      "sEmail": "ava@example.com",
      "sPersonOwner": "string",
      "sPhone": "string",
      "sProject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fDeleted` | boolean | Whether the project is deleted. |
| `fInbox` | boolean | Whether the project is the inbox project. |
| `ixPersonOwner` | number | Owner person ID. |
| `ixProject` | number | Project ID. |
| `ixWorkflow` | number | Workflow ID. |
| `sEmail` | string | Project contact email. |
| `sPersonOwner` | string | Owner name. |
| `sPhone` | string | Project contact phone. |
| `sProject` | string | Project name. |

## Native endpoint

Through the native FogBugz API, this operation is `POST /listProjects` (base URL `{{credentials.siteUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

