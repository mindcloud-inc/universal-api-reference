# Port API AI: Get Blueprint Entity Count

Retrieves a blueprint's entity count from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-blueprint-entity-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-blueprint-entity-count?connectionId=$CONNECTION_ID&blueprintIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blueprintIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-blueprint-entity-count?${params}`, {
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
| `blueprintIdentifier` | string | yes | The blueprint identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `GET /blueprints/:blueprint_identifier/entities-count` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-blueprint-entity-count.md) for the provider-specific parameters and requirements.

