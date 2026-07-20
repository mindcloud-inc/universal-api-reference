# Datumbox: Text Extraction

Extracts clear text from HTML in Datumbox.

```
GET https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/text-extraction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datumbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/text-extraction?connectionId=$CONNECTION_ID&text=Paste%20the%20HTML%20source%20of%20the%20webpage." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Paste the HTML source of the webpage."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/text-extraction?${params}`, {
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
| `text` | string | yes | The HTML source of the webpage to extract text from. Example: `Paste the HTML source of the webpage.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | The extracted clear text from the supplied HTML source. |
| `status` | number | Datumbox success flag for the operation. |

## Native endpoint

Through the native Datumbox API, this operation is `POST /TextExtraction.json` (base URL `http://api.datumbox.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/text-extraction.md) for the provider-specific parameters and requirements.

