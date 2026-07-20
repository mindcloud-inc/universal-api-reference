# BotStar: List CMS Entity Items



```
GET https://connect.mindcloud.co/v1/universal/botStar/latest/actions/list-cms-entity-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotStar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botStar/latest/actions/list-cms-entity-items?connectionId=$CONNECTION_ID&botId=string&entityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string",
  "entityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botStar/latest/actions/list-cms-entity-items?${params}`, {
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
| `botId` | string | yes |  |
| `entityId` | string | yes |  |
| `env` | string | no |  |
| `page` | number | no |  |
| `limit` | number | no |  |
| `name` | string | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].entity_id` | string |  |
| `[].field_unique_name1` | string |  |
| `[].field_unique_name2[]` | string |  |
| `[].id` | string |  |
| `[].name` | string |  |
| `[].status` | string |  |

## Native endpoint

Through the native BotStar API, this operation is `GET /bots/:botId/cms_entities/:entityId/items` (base URL `https://apis.botstar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cms-entity-items.md) for the provider-specific parameters and requirements.

