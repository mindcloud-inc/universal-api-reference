# Wolfram Alpha: Get Summary Box

Retrieves a summary box from Wolfram Alpha.

```
GET https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-summary-box
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wolfram Alpha `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-summary-box?connectionId=$CONNECTION_ID&path=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-summary-box?${params}`, {
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
| `path` | string | yes | Summary box path returned by the Fast Query Recognizer or documented path values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string",
      "path": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string | Summary box HTML content. |
| `path` | string | Requested summary box path. |
| `title` | string | Summary box title when available. |

## Native endpoint

Through the native Wolfram Alpha API, this operation is `GET https://www.wolframalpha.com/summaryboxes/v1/query` (base URL `https://api.wolframalpha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-summary-box.md) for the provider-specific parameters and requirements.

