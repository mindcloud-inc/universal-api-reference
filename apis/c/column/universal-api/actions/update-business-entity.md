# Column: Update Business Entity



```
PUT https://connect.mindcloud.co/v1/universal/column/latest/actions/update-business-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/column/latest/actions/update-business-entity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/column/latest/actions/update-business-entity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityId` | string | yes |  |
| `businessName` | string | no |  |
| `ein` | string | no |  |
| `industry` | string | no |  |
| `website` | string | no |  |
| `dbaName` | string | no |  |
| `legalType` | list | no | One of: `Corporation`, `General Partnership`, `Government`, `LLC`, `Limited Partnership`, `Non-Profit`, `Other`, `Professional Association`, `Sole Proprietorship`, `Trust`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Column API returns.

## Native endpoint

Through the native Column API, this operation is `PATCH /entities/business/:entity_id` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-business-entity.md) for the provider-specific parameters and requirements.

