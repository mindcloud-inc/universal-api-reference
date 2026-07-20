# Port API AI: Update Auto Discovery Suggestion



```
PUT https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-auto-discovery-suggestion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-auto-discovery-suggestion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityIdentifier": "string",
  "invocationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-auto-discovery-suggestion', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityIdentifier": "string",
    "invocationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blueprint` | string | no | Suggested blueprint identifier. |
| `entityIdentifier` | string | yes | The entity identifier. |
| `identifier` | string | no | Suggested entity identifier. |
| `invocationId` | string | yes | The auto-discovery invocation identifier. |
| `title` | string | no | Suggested entity title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Port API AI API, this operation is `PATCH /ai/entities-auto-discovery/:invocation_id/suggestions/:entity_identifier` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-auto-discovery-suggestion.md) for the provider-specific parameters and requirements.

