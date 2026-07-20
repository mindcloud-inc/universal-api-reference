# Chaindesk: List Datastores

Retrieves datastores from your Chaindesk workspace.

```
GET https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-datastores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-datastores?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-datastores?${params}`, {
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
      "_count": {
        "datasources": 1
      },
      "config": {},
      "createdAt": "string",
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
| `config` | object |  |
| `createdAt` | string |  |
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

Through the native Chaindesk API, this operation is `GET /datastores` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-datastores.md) for the provider-specific parameters and requirements.

