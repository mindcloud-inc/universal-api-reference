# Cat Facts: Get Random Fact



```
GET https://connect.mindcloud.co/v1/universal/catFacts/latest/actions/get-random-fact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cat Facts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/catFacts/latest/actions/get-random-fact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/catFacts/latest/actions/get-random-fact?${params}`, {
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
| `max_length` | number | no | Maximum length of the returned fact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fact": "string",
      "length": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fact` | string | Cat fact text. |
| `length` | number | Length of the fact. |

## Native endpoint

Through the native Cat Facts API, this operation is `GET /fact` (base URL `https://catfact.ninja`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-fact.md) for the provider-specific parameters and requirements.

