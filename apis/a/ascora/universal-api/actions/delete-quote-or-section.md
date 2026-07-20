# Ascora: Delete Quote Or Section

Deletes a quote or quote section from Ascora.

```
DELETE https://connect.mindcloud.co/v1/universal/ascora/latest/actions/delete-quote-or-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/delete-quote-or-section?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/delete-quote-or-section?${params}`, {
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
| `quoteNumber` | string | no | Quotation or quotation section number to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Ascora delete result message. |
| `success` | boolean | Whether Ascora deleted the quote or section. |

## Native endpoint

Through the native Ascora API, this operation is `POST /Quotes/DeleteQuote` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-quote-or-section.md) for the provider-specific parameters and requirements.

