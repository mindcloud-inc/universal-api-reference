# Chat Aid: Submit Question

Submits a question to Chat Aid for asynchronous completion.

```
GET https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/submit-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chat Aid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/submit-question?connectionId=$CONNECTION_ID&prompt=What%20is%20our%20refund%20policy%3F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "prompt": "What is our refund policy?"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/submit-question?${params}`, {
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
| `prompt` | string | yes | The question to answer. Example: `What is our refund policy?`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parentTs` | string | no | Unix timestamp used to maintain conversation context across multiple questions. Example: `1640995200`. |
| `messageTs` | string | no | Unix timestamp of the current message for a follow-up question. Example: `1640995260`. |
| `wikiFilters.teams[]` | array<string> | no | Team IDs to restrict the search scope within the teams accessible to the API key. Example: `team-id-1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "pollEndpoint": "string",
      "promptId": "string",
      "timeInterval": 1,
      "votingEndpoint": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `pollEndpoint` | string |  |
| `promptId` | string |  |
| `timeInterval` | number |  |
| `votingEndpoint` | string |  |

## Native endpoint

Through the native Chat Aid API, this operation is `POST /chat/completions/custom` (base URL `https://api.chataid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-question.md) for the provider-specific parameters and requirements.

