# icanhazdadjoke: Fetch Random Slack Dad Joke

Retrieves a random dad joke from icanhazdadjoke formatted for Slack.

```
GET https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/fetch-random-slack-dad-joke
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a icanhazdadjoke `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/fetch-random-slack-dad-joke?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/fetch-random-slack-dad-joke?${params}`, {
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
      "attachments": [
        {}
      ],
      "response_type": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> | Slack attachment payloads containing the joke text and fallback. |
| `response_type` | string | Slack response visibility type. |
| `username` | string | Slack message username. |

## Native endpoint

Through the native icanhazdadjoke API, this operation is `GET /slack` (base URL `https://icanhazdadjoke.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-random-slack-dad-joke.md) for the provider-specific parameters and requirements.

