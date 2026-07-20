# Bookoly: Get Speech Dialogue

Retrieves a specific speech dialogue from Bookoly.

```
GET https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/get-speech-dialogue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookoly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/get-speech-dialogue?connectionId=$CONNECTION_ID&speechDialogue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "speechDialogue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/get-speech-dialogue?${params}`, {
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
| `speechDialogue` | string | yes | The speech dialogue ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bookoly API returns.

## Native endpoint

Through the native Bookoly API, this operation is `GET /speechDialogues/{speechDialogue}` (base URL `https://bookoly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-speech-dialogue.md) for the provider-specific parameters and requirements.

