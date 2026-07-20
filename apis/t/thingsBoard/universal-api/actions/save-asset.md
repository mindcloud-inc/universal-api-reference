# ThingsBoard: Save Asset

Creates or updates an asset in ThingsBoard.

```
PUT https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/save-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/save-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/save-asset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "assetProfileId": {
        "id": "string"
      },
      "createdTime": 1,
      "id": {
        "entityType": "string",
        "id": "string"
      },
      "label": "string",
      "name": "Ava Chen",
      "tenantId": {
        "id": "string"
      },
      "type": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetProfileId.id` | string |  |
| `createdTime` | number |  |
| `id.entityType` | string |  |
| `id.id` | string |  |
| `label` | string |  |
| `name` | string |  |
| `tenantId.id` | string |  |
| `type` | string |  |
| `version` | number |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `POST /asset` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-asset.md) for the provider-specific parameters and requirements.

