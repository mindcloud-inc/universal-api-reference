# Port API AI: List Blueprint Entities

Retrieves entities from a Port blueprint.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/list-blueprint-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/list-blueprint-entities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/list-blueprint-entities?${params}`, {
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
| `blueprintIdentifier` | string | no | The Port blueprint identifier. |

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

Through the native Port API AI API, this operation is `GET /blueprints/:blueprint_identifier/entities` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-blueprint-entities.md) for the provider-specific parameters and requirements.

