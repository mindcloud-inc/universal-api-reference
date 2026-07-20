# BotStar: Create CMS Entity



```
POST https://connect.mindcloud.co/v1/universal/botStar/latest/actions/create-cms-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotStar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botStar/latest/actions/create-cms-entity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botStar/latest/actions/create-cms-entity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string",
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
| `env` | string | no |  |
| `name` | string | yes |  |
| `fields[]` | array<object> | no | Optional array of CMS field objects to create with the entity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {
          "data_type": "string",
          "name": "Ava Chen",
          "options": {
            "entity_id": "string",
            "predefined_data": [
              {
                "label": "string",
                "value": "string"
              }
            ]
          },
          "unique_name": "Ava Chen"
        }
      ],
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields[].data_type` | string |  |
| `fields[].name` | string |  |
| `fields[].options.entity_id` | string |  |
| `fields[].options.predefined_data[].label` | string |  |
| `fields[].options.predefined_data[].value` | string |  |
| `fields[].unique_name` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native BotStar API, this operation is `POST /bots/:botId/cms_entities` (base URL `https://apis.botstar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-cms-entity.md) for the provider-specific parameters and requirements.

