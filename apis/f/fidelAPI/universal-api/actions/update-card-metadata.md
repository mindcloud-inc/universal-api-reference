# Fidel API: Update Card Metadata

Updates metadata for a Fidel card.

```
PUT https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-card-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-card-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-card-metadata', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {
        "codexStage3": "string",
        "updatedBy": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata.codexStage3` | string |  |
| `metadata.updatedBy` | string |  |

## Native endpoint

Through the native Fidel API API, this operation is `PUT /cards/:cardId/metadata` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-card-metadata.md) for the provider-specific parameters and requirements.

