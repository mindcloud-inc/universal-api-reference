# BotStar: Create CMS Entity Item



```
POST https://connect.mindcloud.co/v1/universal/botStar/latest/actions/create-cms-entity-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotStar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botStar/latest/actions/create-cms-entity-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string",
  "entityId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botStar/latest/actions/create-cms-entity-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string",
    "entityId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes |  |
| `entityId` | string | yes |  |
| `env` | string | no |  |
| `name` | string | yes |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entity_id": "string",
      "field_unique_name1": "Ava Chen",
      "field_unique_name2": [
        "Ava Chen"
      ],
      "id": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity_id` | string |  |
| `field_unique_name1` | string |  |
| `field_unique_name2[]` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native BotStar API, this operation is `POST /bots/:botId/cms_entities/:entityId/items` (base URL `https://apis.botstar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-cms-entity-item.md) for the provider-specific parameters and requirements.

