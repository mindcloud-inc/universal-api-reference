# Chaindesk: Get Datastore

Retrieves an existing datastore from Chaindesk.

```
GET https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/get-datastore
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/get-datastore?connectionId=$CONNECTION_ID&datastoreId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datastoreId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/get-datastore?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datastoreId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_count": {
        "datasources": 1
      },
      "apiKeys": {
        "createdAt": "string",
        "datastoreId": "string",
        "id": "string",
        "key": "string"
      },
      "config": {},
      "createdAt": "string",
      "datasources": {
        "_count": {
          "children": 1
        },
        "children": [
          "string"
        ],
        "config": {
          "tags": [
            "string"
          ],
          "text": "string"
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
      },
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "ownerId": "string",
      "pluginDescriptionForHumans": "string",
      "pluginDescriptionForModel": "string",
      "pluginIconUrl": "https://example.com",
      "pluginName": "Ava Chen",
      "type": "string",
      "updatedAt": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_count` | object |  |
| `_count.datasources` | number |  |
| `apiKeys` | array<object> |  |
| `apiKeys.createdAt` | string |  |
| `apiKeys.datastoreId` | string |  |
| `apiKeys.id` | string |  |
| `apiKeys.key` | string |  |
| `config` | object |  |
| `createdAt` | string |  |
| `datasources` | array<object> |  |
| `datasources._count` | object |  |
| `datasources._count.children` | number |  |
| `datasources.children` | array<string> |  |
| `datasources.config` | object |  |
| `datasources.config.tags` | array<string> |  |
| `datasources.config.text` | string |  |
| `datasources.createdAt` | string |  |
| `datasources.datastoreId` | string |  |
| `datasources.groupId` | string |  |
| `datasources.hash` | string |  |
| `datasources.id` | string |  |
| `datasources.lastSynch` | string |  |
| `datasources.name` | string |  |
| `datasources.nbChunks` | number |  |
| `datasources.nbSynch` | number |  |
| `datasources.nbTokens` | number |  |
| `datasources.organizationId` | string |  |
| `datasources.ownerId` | string |  |
| `datasources.serviceProviderId` | string |  |
| `datasources.status` | string |  |
| `datasources.textSize` | number |  |
| `datasources.type` | string |  |
| `datasources.updatedAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `ownerId` | string |  |
| `pluginDescriptionForHumans` | string |  |
| `pluginDescriptionForModel` | string |  |
| `pluginIconUrl` | string |  |
| `pluginName` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Chaindesk API, this operation is `GET /datastores/:datastoreId` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-datastore.md) for the provider-specific parameters and requirements.

