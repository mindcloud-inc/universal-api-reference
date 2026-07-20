# Port API AI: Get Entity Properties History

Retrieves entity property history from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-entity-properties-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-entity-properties-history?connectionId=$CONNECTION_ID&blueprintIdentifier=string&entityIdentifier=string&propertyNames%5B%5D=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blueprintIdentifier": "string",
  "entityIdentifier": "string",
  "propertyNames[]": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-entity-properties-history?${params}`, {
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
| `blueprintIdentifier` | string | yes | Blueprint identifier. |
| `entityIdentifier` | string | yes | Entity identifier. |
| `propertyNames[]` | array<string> | yes | Properties to fetch history for. |

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

Through the native Port API AI API, this operation is `POST /entities/properties-history` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-entity-properties-history.md) for the provider-specific parameters and requirements.

