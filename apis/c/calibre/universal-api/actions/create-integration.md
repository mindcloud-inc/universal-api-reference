# Calibre: Create Integration

Creates a new integration in Calibre.

```
POST https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.site": "string",
  "variables.provider": "webhook",
  "variables.url": "https://example.com/webhook",
  "variables.event": "new_snapshot"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-integration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.site": "string",
    "variables.provider": "webhook",
    "variables.url": "https://example.com/webhook",
    "variables.event": "new_snapshot"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.site` | string | yes |  |
| `variables.provider` | string | yes | Default: `webhook`. |
| `variables.url` | string | yes | Example: `https://example.com/webhook`. |
| `variables.event` | string<string> | yes | Default: `new_snapshot`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.secret` | string | no |  |
| `variables.isDisabled` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createIntegration": {
        "events": [
          "string"
        ],
        "isDisabled": true,
        "provider": "string",
        "secret": "string",
        "url": "https://example.com",
        "uuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createIntegration.events[]` | string |  |
| `createIntegration.isDisabled` | boolean |  |
| `createIntegration.provider` | string |  |
| `createIntegration.secret` | string |  |
| `createIntegration.url` | string |  |
| `createIntegration.uuid` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-integration.md) for the provider-specific parameters and requirements.

