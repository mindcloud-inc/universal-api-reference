# Statsig: Create Dynamic Config

Creates a dynamic config in Statsig.

```
POST https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-dynamic-config-post-console-v1-dynamic-configs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-dynamic-config-post-console-v1-dynamic-configs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-dynamic-config-post-console-v1-dynamic-configs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Request body field. |
| `isEnabled` | boolean | no | Request body field. |
| `description` | string | no | Request body field. |
| `rules` | list | no | Request body field. |
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
| `id` | string | no | Request body field. |
| `isTemplate` | boolean | no | Request body field. |

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

Through the native Statsig API, this operation is `POST /console/v1/dynamic_configs` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dynamic-config-post-console-v1-dynamic-configs.md) for the provider-specific parameters and requirements.

