# Humor API: Submit Joke



```
POST https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/submit-joke
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Humor API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/submit-joke" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/submit-joke', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jokeText` | string | no | The joke text to submit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "joke": {
        "id": 1,
        "joke": "string",
        "tags": [
          "string"
        ]
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `joke.id` | number |  |
| `joke.joke` | string |  |
| `joke.tags[]` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Humor API API, this operation is `POST /jokes` (base URL `https://api.humorapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-joke.md) for the provider-specific parameters and requirements.

