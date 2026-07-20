# Chaindesk: Create Text Datasource

Creates a text datasource in Chaindesk.

```
POST https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-text-datasource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-text-datasource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datastoreId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-text-datasource', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datastoreId": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datastoreId` | string | yes |  |
| `text` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {
        "tags": [
          "string"
        ]
      },
      "createdAt": "string",
      "datastoreId": "string",
      "groupId": "string",
      "hash": "string",
      "id": "string",
      "lastSynch": "string",
      "name": "Ava Chen",
      "nbChunks": 1,
      "nbSynch": 1,
      "nbTokens": 1,
      "organizationId": "string",
      "ownerId": "string",
      "serviceProviderId": "string",
      "status": "string",
      "textSize": 1,
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
| `config` | object |  |
| `config.tags` | array<string> |  |
| `createdAt` | string |  |
| `datastoreId` | string |  |
| `groupId` | string |  |
| `hash` | string |  |
| `id` | string |  |
| `lastSynch` | string |  |
| `name` | string |  |
| `nbChunks` | number |  |
| `nbSynch` | number |  |
| `nbTokens` | number |  |
| `organizationId` | string |  |
| `ownerId` | string |  |
| `serviceProviderId` | string |  |
| `status` | string |  |
| `textSize` | number |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Chaindesk API, this operation is `POST /datasources` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-datasource.md) for the provider-specific parameters and requirements.

