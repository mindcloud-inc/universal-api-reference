# Bump.sh: Create Version

Creates a new documentation version in Bump.sh.

```
POST https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/create-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bump.sh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/create-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentation": "string",
  "definition": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/create-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentation": "string",
    "definition": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branch_name` | string | no | Branch name for the new version. Defaults to the main branch if omitted. |
| `documentation` | string | yes | UUID or slug of the documentation. |
| `hub` | string | no | Hub ID or slug when auto-creating a documentation inside a hub. |
| `previous_version_id` | string | no | Existing version ID used as the previous deployed version reference. |
| `documentationName` | string | no | Name to use when auto-creating the documentation. |
| `autoCreateDocumentation` | boolean | no | Create the documentation if it does not exist yet. Default: `true`. |
| `definition` | string | yes | Serialized OpenAPI or AsyncAPI definition string. |
| `temporary` | boolean | no | Create the version as a temporary change with a 7 day TTL. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bump.sh API returns.

## Native endpoint

Through the native Bump.sh API, this operation is `POST versions` (base URL `https://bump.sh/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-version.md) for the provider-specific parameters and requirements.

