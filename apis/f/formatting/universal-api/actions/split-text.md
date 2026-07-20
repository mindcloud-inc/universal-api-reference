# Formatting: Split Text

Splits text into segments in the Formatting app.

```
GET https://connect.mindcloud.co/v1/universal/formatting/latest/actions/split-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formatting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formatting/latest/actions/split-text?connectionId=$CONNECTION_ID&input=string&separator=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string",
  "separator": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formatting/latest/actions/split-text?${params}`, {
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
| `input` | string | yes | The text to split. |
| `separator` | string | yes | The separator string. |
| `segmentIndex` | number | no | The zero-based segment index to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "segments": [
        "string"
      ],
      "selectedSegment": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `segments` | array<string> |  |
| `selectedSegment` | string |  |

## Native endpoint

Through the native Formatting API, this operation is `POST /post` (base URL `https://postman-echo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-text.md) for the provider-specific parameters and requirements.

