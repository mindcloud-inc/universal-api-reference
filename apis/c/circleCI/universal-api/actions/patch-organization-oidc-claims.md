# CircleCI: Patch Organization OIDC Claims



```
PUT https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/patch-organization-oidc-claims
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/patch-organization-oidc-claims" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orgID": "afbcafd1-31ea-4324-bc26-bf5d7e8e3e16"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/patch-organization-oidc-claims', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orgID": "afbcafd1-31ea-4324-bc26-bf5d7e8e3e16"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orgID` | string | yes | The CircleCI organization UUID. Default: `afbcafd1-31ea-4324-bc26-bf5d7e8e3e16`. |
| `ttl` | string | no | OIDC token TTL duration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audience": [
        "string"
      ],
      "audienceUpdatedAt": "string",
      "orgId": "string",
      "projectId": "string",
      "ttl": "string",
      "ttlUpdatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audience` | array<string> |  |
| `audienceUpdatedAt` | string |  |
| `orgId` | string |  |
| `projectId` | string |  |
| `ttl` | string |  |
| `ttlUpdatedAt` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `PATCH /org/:orgID/oidc-custom-claims` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-organization-oidc-claims.md) for the provider-specific parameters and requirements.

