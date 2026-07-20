# Statsig: Fully Update Dynamic Config

Updates a dynamic config in Statsig.

```
PUT https://connect.mindcloud.co/v1/universal/statsig/latest/actions/fully-update-dynamic-config-post-console-v1-dynamic-configs-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/fully-update-dynamic-config-post-console-v1-dynamic-configs-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "isEnabled": true,
  "description": "string",
  "rules": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/fully-update-dynamic-config-post-console-v1-dynamic-configs-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "isEnabled": true,
    "description": "string",
    "rules": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | id |
| `name` | string | no | Request body field. |
| `isEnabled` | boolean | yes | Request body field. |
| `description` | string | yes | Request body field. |
| `rules` | list | yes | Request body field. |
| `defaultValue` | object | no | Request body field. |
| `defaultValueJson5` | string | no | Request body field. |
| `idType` | string | no | Request body field. |
| `tags` | list | no | Request body field. |
| `creatorID` | string | no | Request body field. |
| `owner` | object | no | Request body field. |
| `creatorEmail` | string | no | Request body field. |
| `schema` | string | no | Request body field. |
| `schemaJson5` | string | no | Request body field. |
| `targetApps` | string | no | Request body field. |
| `team` | string | no | Request body field. |
| `teamID` | string | no | Request body field. |
| `releasePipelineID` | string | no | Request body field. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dryRun` | boolean | no | Skips persisting updates to the entity (used to validate that inputs are correct) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `POST /console/v1/dynamic_configs/{id}` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fully-update-dynamic-config-post-console-v1-dynamic-configs-id.md) for the provider-specific parameters and requirements.

