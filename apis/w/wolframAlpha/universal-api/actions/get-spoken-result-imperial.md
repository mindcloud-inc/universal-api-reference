# Wolfram Alpha: Get Spoken Result Imperial

Retrieves a spoken imperial answer from Wolfram Alpha.

```
GET https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-spoken-result-imperial
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wolfram Alpha `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-spoken-result-imperial?connectionId=$CONNECTION_ID&i=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "i": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-spoken-result-imperial?${params}`, {
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
| `i` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "query": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `query` | string | Original query text. |
| `result` | string | Spoken plain-text answer returned by Wolfram\|Alpha. |

## Native endpoint

Through the native Wolfram Alpha API, this operation is `GET /v1/spoken` (base URL `https://api.wolframalpha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-spoken-result-imperial.md) for the provider-specific parameters and requirements.

