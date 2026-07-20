# Vistaly: Search Cards

Finds cards in Vistaly by semantic search.

```
GET https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/search-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vistaly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/search-cards?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/search-cards?${params}`, {
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
| `query` | string | yes | Natural language search query that finds cards with similar content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | object | no | Optional filter object with must, must_not, and should clauses for card metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
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
| `results` | array<object> |  |

## Native endpoint

Through the native Vistaly API, this operation is `POST /beta/cards/search` (base URL `https://api.vistaly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-cards.md) for the provider-specific parameters and requirements.

