# Chaindesk: Create S3 Datastore

Creates an S3 datastore in Chaindesk.

```
POST https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-s3-datastore
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-s3-datastore" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-s3-datastore', {
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
| `name` | string | yes |  |

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

Through the native Chaindesk API, this operation is `POST /datastores` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-s3-datastore.md) for the provider-specific parameters and requirements.

