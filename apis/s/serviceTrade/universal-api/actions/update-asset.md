# ServiceTrade: Update Asset

Updates an existing asset in ServiceTrade.

```
PUT https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/update-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTrade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/update-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assetId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/update-asset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assetId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assetId` | number | yes | Asset to update. |
| `properties.notes` | string | no | Updated notes for asset definitions that support it. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskListId` | number | no | Updated task list for the asset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assetDefinition": {
        "display": "string",
        "id": 1,
        "type": "string"
      },
      "created": 1,
      "display": "string",
      "externalIds": {
        "quickbooks": "string"
      },
      "hasActiveTaskList": true,
      "id": 1,
      "isAbstractGroup": true,
      "legacyId": "string",
      "location": {
        "address": {
          "city": "string",
          "state": "string"
        },
        "id": 1,
        "name": "Ava Chen",
        "refNumber": "string",
        "status": "string"
      },
      "name": "Ava Chen",
      "orderIndex": 1,
      "parent": {
        "id": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "serviceLine": {
        "abbr": "string",
        "id": 1,
        "name": "Ava Chen",
        "trade": "string"
      },
      "status": "string",
      "type": "string",
      "updated": 1,
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetDefinition.display` | string |  |
| `assetDefinition.id` | number |  |
| `assetDefinition.type` | string |  |
| `created` | number |  |
| `display` | string |  |
| `externalIds.quickbooks` | string |  |
| `hasActiveTaskList` | boolean |  |
| `id` | number |  |
| `isAbstractGroup` | boolean |  |
| `legacyId` | string |  |
| `location.address.city` | string |  |
| `location.address.state` | string |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `location.refNumber` | string |  |
| `location.status` | string |  |
| `name` | string |  |
| `orderIndex` | number |  |
| `parent.id` | number |  |
| `parent.name` | string |  |
| `parent.type` | string |  |
| `serviceLine.abbr` | string |  |
| `serviceLine.id` | number |  |
| `serviceLine.name` | string |  |
| `serviceLine.trade` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updated` | number |  |
| `uri` | string |  |

## Native endpoint

Through the native ServiceTrade API, this operation is `PUT asset/:assetId` (base URL `https://api.servicetrade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-asset.md) for the provider-specific parameters and requirements.

