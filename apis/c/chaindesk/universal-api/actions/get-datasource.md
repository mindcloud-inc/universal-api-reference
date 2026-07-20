# Chaindesk: Get Datasource

Retrieves an existing datasource from Chaindesk.

```
GET https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/get-datasource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/get-datasource?connectionId=$CONNECTION_ID&datasourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/get-datasource?${params}`, {
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
| `datasourceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {
        "source_url": "https://example.com",
        "tags": [
          "string"
        ]
      },
      "createdAt": "string",
      "datastore": {
        "name": "Ava Chen"
      },
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
| `config.source_url` | string |  |
| `config.tags` | array<string> |  |
| `createdAt` | string |  |
| `datastore` | object |  |
| `datastore.name` | string |  |
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

Through the native Chaindesk API, this operation is `GET /datasources/:datasourceId` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-datasource.md) for the provider-specific parameters and requirements.

