# Tisane Labs: List Inflected Forms

Retrieves inflected forms from Tisane Labs.

```
GET https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/list-inflected-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tisane Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/list-inflected-forms?connectionId=$CONNECTION_ID&language=en&lexeme=12345&family=67890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "language": "en",
  "lexeme": "12345",
  "family": "67890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/list-inflected-forms?${params}`, {
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
| `language` | string | yes | Code of a language in Tisane, for example en. Example: `en`. |
| `lexeme` | string | yes | ID of the lexeme to inspect. Example: `12345`. |
| `family` | string | yes | ID of the family to inspect. Example: `67890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "features": [
        {}
      ],
      "isLemma": true,
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `features` | array<object> | Feature index/value pairs for the inflected form. |
| `isLemma` | boolean | Whether the form is the lemma. |
| `text` | string | Inflected form text. |

## Native endpoint

Through the native Tisane Labs API, this operation is `GET /lm/inflections` (base URL `https://api.tisane.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inflected-forms.md) for the provider-specific parameters and requirements.

