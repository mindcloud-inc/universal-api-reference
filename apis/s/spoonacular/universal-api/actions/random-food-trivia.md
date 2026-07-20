# Spoonacular: Random Food Trivia

Retrieves random food trivia from Spoonacular.

```
GET https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/random-food-trivia
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/random-food-trivia?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/random-food-trivia?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `text` | string |  |

## Native endpoint

Through the native Spoonacular API, this operation is `GET /food/trivia/random` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/random-food-trivia.md) for the provider-specific parameters and requirements.

