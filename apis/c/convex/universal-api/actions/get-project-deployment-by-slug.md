# Convex: Get Project Deployment By Slug

Retrieves a deployment from Convex by project slug.

```
GET https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-project-deployment-by-slug
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-project-deployment-by-slug?connectionId=$CONNECTION_ID&teamIdOrSlug=string&projectSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamIdOrSlug": "string",
  "projectSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-project-deployment-by-slug?${params}`, {
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
| `teamIdOrSlug` | string | yes | The Convex team ID or slug. |
| `projectSlug` | string | yes | The Convex project slug. |
| `reference` | string | no | The deployment reference to fetch. |
| `defaultProd` | boolean | no | Fetch the default production deployment for the caller. |
| `defaultDev` | boolean | no | Fetch the default development deployment for the caller. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "class": "string",
      "createTime": 1,
      "creator": 1,
      "dashboardEditConfirmation": "string",
      "deploymentType": "string",
      "deploymentUrl": "https://example.com",
      "id": 1,
      "isDefault": true,
      "kind": "string",
      "name": "Ava Chen",
      "previewIdentifier": "string",
      "projectId": 1,
      "reference": "string",
      "region": "string",
      "sendLogsToClient": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `class` | string |  |
| `createTime` | number |  |
| `creator` | number |  |
| `dashboardEditConfirmation` | string |  |
| `deploymentType` | string |  |
| `deploymentUrl` | string |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `kind` | string |  |
| `name` | string |  |
| `previewIdentifier` | string |  |
| `projectId` | number |  |
| `reference` | string |  |
| `region` | string |  |
| `sendLogsToClient` | boolean |  |

## Native endpoint

Through the native Convex API, this operation is `GET /teams/:team_id_or_slug/projects/:project_slug/deployment` (base URL `https://api.convex.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-deployment-by-slug.md) for the provider-specific parameters and requirements.

