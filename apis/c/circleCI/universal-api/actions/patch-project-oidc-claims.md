# CircleCI: Patch Project OIDC Claims



```
PUT https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/patch-project-oidc-claims
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/patch-project-oidc-claims" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/patch-project-oidc-claims', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audience` | string | no | OIDC audience value. |
| `orgID` | string | no | Opaque organization identifier. |
| `projectID` | string | no | Opaque project identifier. |
| `ttl` | number | no | OIDC token TTL in seconds. |

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

Through the native CircleCI API, this operation is `PATCH /org/:orgID/project/:projectID/oidc-custom-claims` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-project-oidc-claims.md) for the provider-specific parameters and requirements.

