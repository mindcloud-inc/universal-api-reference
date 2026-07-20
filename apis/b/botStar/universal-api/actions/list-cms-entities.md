# BotStar: List CMS Entities



```
GET https://connect.mindcloud.co/v1/universal/botStar/latest/actions/list-cms-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotStar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botStar/latest/actions/list-cms-entities?connectionId=$CONNECTION_ID&botId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botStar/latest/actions/list-cms-entities?${params}`, {
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
| `env` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].fields[].data_type` | string |  |
| `[].fields[].name` | string |  |
| `[].fields[].options.entity_id` | string |  |
| `[].fields[].options.predefined_data[].label` | string |  |
| `[].fields[].options.predefined_data[].value` | string |  |
| `[].fields[].unique_name` | string |  |
| `[].id` | string |  |
| `[].name` | string |  |

## Native endpoint

Through the native BotStar API, this operation is `GET /bots/:botId/cms_entities` (base URL `https://apis.botstar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cms-entities.md) for the provider-specific parameters and requirements.

