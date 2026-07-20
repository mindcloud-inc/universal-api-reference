# Chaindesk: Delete Datastore

Deletes an existing datastore from Chaindesk.

```
DELETE https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/delete-datastore
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/delete-datastore?connectionId=$CONNECTION_ID&datastoreId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datastoreId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/delete-datastore?${params}`, {
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

Through the native Chaindesk API, this operation is `DELETE /datastores/:datastoreId` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-datastore.md) for the provider-specific parameters and requirements.

