# BotStar: Create CMS Entity Fields



```
POST https://connect.mindcloud.co/v1/universal/botStar/latest/actions/create-cms-entity-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotStar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botStar/latest/actions/create-cms-entity-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string",
  "entityId": "string",
  "fields[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botStar/latest/actions/create-cms-entity-fields', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string",
    "entityId": "string",
    "fields[]": [{}]
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
| `fields[]` | array<object> | yes | Array of CMS field objects to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native BotStar API, this operation is `POST /bots/:botId/cms_entities/:entityId/fields` (base URL `https://apis.botstar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-cms-entity-fields.md) for the provider-specific parameters and requirements.

