# openpm: Update Package



```
PUT https://connect.mindcloud.co/v1/universal/openpm/latest/actions/update-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a openpm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/openpm/latest/actions/update-package" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": "string",
  "id": "string",
  "openapi": "string",
  "oauthClientId": "string",
  "oauthClientSecret": "string",
  "oauthAuthorizationUrl": "https://example.com",
  "oauthTokenUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openpm/latest/actions/update-package', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": "string",
    "id": "string",
    "openapi": "string",
    "oauthClientId": "string",
    "oauthClientSecret": "string",
    "oauthAuthorizationUrl": "https://example.com",
    "oauthTokenUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | string | yes | Package ID. |
| `id` | string | yes | Package ID. |
| `name` | string | no | Package name. |
| `machineName` | string | no | Package name for machines. |
| `domain` | string | no | Package domain. |
| `version` | string | no | Package version. |
| `logoUrl` | string | no | Package logo URL. |
| `contactEmail` | string | no | Package contact email. |
| `legalInfoUrl` | string | no | Package legal info URL. |
| `description` | string | no | Package description. |
| `machineDescription` | string | no | Package description for machines. |
| `openapi` | string | yes | Package OpenAPI specification. Runtime validation requires the OpenAPI document to include a server URL/domain. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `oauthClientId` | string | yes | OAuth client ID required by OpenPM when updating a package. |
| `oauthClientSecret` | string | yes | OAuth client secret required by OpenPM when updating a package. |
| `oauthAuthorizationUrl` | string | yes | OAuth authorization URL required by OpenPM when updating a package. |
| `oauthTokenUrl` | string | yes | OAuth token URL required by OpenPM when updating a package. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Updated package id. |

## Native endpoint

Through the native openpm API, this operation is `PUT /packages/:packageId` (base URL `https://openpm.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-package.md) for the provider-specific parameters and requirements.

