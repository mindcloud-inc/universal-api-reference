# Port API AI: Search Blueprint Entities

Finds entities in a Port blueprint.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/search-blueprint-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/search-blueprint-entities?connectionId=$CONNECTION_ID&blueprintIdentifier=string&query=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blueprintIdentifier": "string",
  "query": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/search-blueprint-entities?${params}`, {
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
| `blueprintIdentifier` | string | yes | The Port blueprint identifier. |
| `query` | object | yes | Blueprint entity query |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entities": [
        {}
      ],
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entities` | array<object> |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /blueprints/:blueprint_identifier/entities/search` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-blueprint-entities.md) for the provider-specific parameters and requirements.

