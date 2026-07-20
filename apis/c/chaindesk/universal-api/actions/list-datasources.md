# Chaindesk: List Datasources

Retrieves datasources from your Chaindesk workspace.

```
GET https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-datasources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-datasources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-datasources?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Chaindesk API, this operation is `GET /datasources` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-datasources.md) for the provider-specific parameters and requirements.

