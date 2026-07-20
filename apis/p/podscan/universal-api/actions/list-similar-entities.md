# Podscan: List Similar Entities

Retrieves similar entity matches from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-similar-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-similar-entities?connectionId=$CONNECTION_ID&entityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-similar-entities?${params}`, {
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
| `entityId` | string | yes | The entity ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entity_id": "string",
      "similar_entities": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity_id` | string |  |
| `similar_entities` | array<object> |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /entities/{entityId}/similar` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-similar-entities.md) for the provider-specific parameters and requirements.

