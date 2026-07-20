# openpm: Create Package



```
POST https://connect.mindcloud.co/v1/universal/openpm/latest/actions/create-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a openpm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openpm/latest/actions/create-package" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "openapi": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openpm/latest/actions/create-package', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "openapi": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "openapi": {},
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Package id. |
| `openapi` | object | Created package OpenAPI specification object. |
| `version` | string | Package version. |

## Native endpoint

Through the native openpm API, this operation is `POST /packages` (base URL `https://openpm.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-package.md) for the provider-specific parameters and requirements.

