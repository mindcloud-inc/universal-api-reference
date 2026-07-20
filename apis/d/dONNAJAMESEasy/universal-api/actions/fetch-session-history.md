# DONNAJAMES Easy: Fetch Session History

Retrieves a session transcript from DONNAJAMES Easy.

```
GET https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/fetch-session-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DONNAJAMES Easy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/fetch-session-history?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/fetch-session-history?${params}`, {
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
| `uuid` | string | yes | Session uuid |

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
| `text` | string | Plain-text session transcript. |

## Native endpoint

Through the native DONNAJAMES Easy API, this operation is `GET session/:uuid/messages/plain-text` (base URL `https://app.gpt-trainer.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-session-history.md) for the provider-specific parameters and requirements.

