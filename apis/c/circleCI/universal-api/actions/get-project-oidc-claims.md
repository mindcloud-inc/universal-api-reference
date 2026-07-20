# CircleCI: Get Project OIDC Claims



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-project-oidc-claims
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-project-oidc-claims?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-project-oidc-claims?${params}`, {
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
      "audience": "string",
      "orgId": "string",
      "projectId": "string",
      "ttl": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audience` | string |  |
| `orgId` | string |  |
| `projectId` | string |  |
| `ttl` | number |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /org/:orgID/project/:projectID/oidc-custom-claims` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-oidc-claims.md) for the provider-specific parameters and requirements.

