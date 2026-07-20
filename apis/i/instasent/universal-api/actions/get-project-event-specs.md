# Instasent: Get Project Event Specs



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-project-event-specs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-project-event-specs?connectionId=$CONNECTION_ID&project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-project-event-specs?${params}`, {
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
| `project` | string | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entities": [
        {
          "attribution": true,
          "automation": true,
          "category": "string",
          "description": "string",
          "emoji": "string",
          "icon": "string",
          "important": true,
          "name": "Ava Chen",
          "uid": "string"
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
| `entities[].attribution` | boolean |  |
| `entities[].automation` | boolean |  |
| `entities[].category` | string |  |
| `entities[].description` | string |  |
| `entities[].emoji` | string |  |
| `entities[].icon` | string |  |
| `entities[].important` | boolean |  |
| `entities[].name` | string |  |
| `entities[].uid` | string |  |

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project/specs/events` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-event-specs.md) for the provider-specific parameters and requirements.

