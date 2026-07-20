# Instasent: Get Event Parameter Specs



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-event-parameter-specs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-event-parameter-specs?connectionId=$CONNECTION_ID&project=string&eventType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "eventType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-event-parameter-specs?${params}`, {
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
| `eventType` | string | yes | Event type slug to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entities": [
        {
          "dataType": "string",
          "description": "string",
          "icon": "string",
          "maxLength": {},
          "multiValue": 1,
          "parameter": "string",
          "required": true,
          "title": "string",
          "visualType": "string"
        }
      ],
      "metadata": {
        "event": {
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
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entities[].dataType` | string |  |
| `entities[].description` | string |  |
| `entities[].icon` | string |  |
| `entities[].maxLength` | object |  |
| `entities[].multiValue` | number |  |
| `entities[].parameter` | string |  |
| `entities[].required` | boolean |  |
| `entities[].title` | string |  |
| `entities[].visualType` | string |  |
| `metadata.event.attribution` | boolean |  |
| `metadata.event.automation` | boolean |  |
| `metadata.event.category` | string |  |
| `metadata.event.description` | string |  |
| `metadata.event.emoji` | string |  |
| `metadata.event.icon` | string |  |
| `metadata.event.important` | boolean |  |
| `metadata.event.name` | string |  |
| `metadata.event.uid` | string |  |

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project/specs/events/:eventType` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-parameter-specs.md) for the provider-specific parameters and requirements.

