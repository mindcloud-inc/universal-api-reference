# Datumbox: Keyword Extraction

Extracts keywords from a document in Datumbox.

```
GET https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/keyword-extraction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datumbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/keyword-extraction?connectionId=$CONNECTION_ID&text=Enter%20the%20text%20to%20analyze%20for%20keyword%20extraction.&n=Enter%20the%20maximum%20n-gram%20size%20to%20extract%2C%20such%20as%202%20or%203." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Enter the text to analyze for keyword extraction.",
  "n": "Enter the maximum n-gram size to extract, such as 2 or 3."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/keyword-extraction?${params}`, {
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
| `text` | string | yes | The clear text to analyze for keyword extraction. Example: `Enter the text to analyze for keyword extraction.`. |
| `n` | number | yes | The maximum keyword-combination size to extract. Example: `Enter the maximum n-gram size to extract, such as 2 or 3.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object | Keyword groups keyed by n-gram size with occurrence counts. |
| `status` | number | Datumbox success flag for the operation. |

## Native endpoint

Through the native Datumbox API, this operation is `POST /KeywordExtraction.json` (base URL `http://api.datumbox.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/keyword-extraction.md) for the provider-specific parameters and requirements.

