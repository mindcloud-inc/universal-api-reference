# Chaindesk: Create Form

Creates a new form in Chaindesk.

```
POST https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "draftConfig": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "draftConfig": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `draftConfig` | object<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "datastoreId": "string",
      "draftConfig": {
        "fields": [
          "string"
        ],
        "schema": {
          "properties": {},
          "required": [
            "string"
          ],
          "type": "string"
        }
      },
      "id": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "publishedConfig": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `datastoreId` | string |  |
| `draftConfig` | object |  |
| `draftConfig.fields` | array<string> |  |
| `draftConfig.schema` | object |  |
| `draftConfig.schema.properties` | object |  |
| `draftConfig.schema.required` | array<string> |  |
| `draftConfig.schema.type` | string |  |
| `id` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `publishedConfig` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Chaindesk API, this operation is `POST /forms` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

