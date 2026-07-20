# CircleCI: Delete Project OIDC Claims



```
DELETE https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/delete-project-oidc-claims
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/delete-project-oidc-claims?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/delete-project-oidc-claims?${params}`, {
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
| `orgID` | string | no | Opaque organization identifier. |
| `projectID` | string | no | Opaque project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "orgId": "string",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `orgId` | string |  |
| `projectId` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `DELETE /org/:orgID/project/:projectID/oidc-custom-claims` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project-oidc-claims.md) for the provider-specific parameters and requirements.

