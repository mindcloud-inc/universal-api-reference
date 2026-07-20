# Instasent: Get Datasource Stream Specs



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-datasource-stream-specs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-datasource-stream-specs?connectionId=$CONNECTION_ID&project=string&datasource=string&spec=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "datasource": "string",
  "spec": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-datasource-stream-specs?${params}`, {
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
| `datasource` | string | yes | Datasource identifier. |
| `spec` | string | yes | Specification identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "specs": [
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
| `specs[].attribution` | boolean |  |
| `specs[].automation` | boolean |  |
| `specs[].category` | string |  |
| `specs[].description` | string |  |
| `specs[].emoji` | string |  |
| `specs[].icon` | string |  |
| `specs[].important` | boolean |  |
| `specs[].name` | string |  |
| `specs[].uid` | string |  |

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project/datasource/:datasource/stream/specs/:spec` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-datasource-stream-specs.md) for the provider-specific parameters and requirements.

