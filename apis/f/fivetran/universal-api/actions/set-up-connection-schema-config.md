# Fivetran: Set Up Connection Schema Config

Creates schema configuration for a connection in Fivetran.

```
POST https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/set-up-connection-schema-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/set-up-connection-schema-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "string",
  "schemas": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/set-up-connection-schema-config', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "connectionId": "string",
    "schemas": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `connectionId` | string | yes | The unique identifier for the connection within Fivetran. |
| `schemaChangeHandling` | string | no | How Fivetran should handle new schemas, tables, and columns. |
| `schemas` | object | yes | The set of schemas within the connection schema config. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "schemaChangeHandling": "string",
      "schemas": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `schemaChangeHandling` | string |  |
| `schemas` | object |  |

## Native endpoint

Through the native Fivetran API, this operation is `POST /connections/[:connectionId]/schemas` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-up-connection-schema-config.md) for the provider-specific parameters and requirements.

