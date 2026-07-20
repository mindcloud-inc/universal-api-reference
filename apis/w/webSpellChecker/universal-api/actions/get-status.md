# WebSpellChecker: Get Status

Retrieves application engine status from WebSpellChecker.

```
GET https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/get-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebSpellChecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/get-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/get-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "EnglishAutocomplete": {
        "active": true,
        "reason": "string"
      },
      "GrammarCheckEngine": {
        "active": true
      },
      "SpellCheckEngine": {
        "active": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `EnglishAutocomplete` | object | English autocomplete engine status. |
| `EnglishAutocomplete.active` | boolean | Whether autocomplete is active. |
| `EnglishAutocomplete.reason` | string | Reason returned when autocomplete is inactive. |
| `GrammarCheckEngine` | object | Grammar-check engine status. |
| `GrammarCheckEngine.active` | boolean | Whether grammar-check is active. |
| `SpellCheckEngine` | object | Spell-check engine status. |
| `SpellCheckEngine.active` | boolean | Whether spell-check is active. |

## Native endpoint

Through the native WebSpellChecker API, this operation is `GET /` (base URL `https://svc.webspellchecker.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-status.md) for the provider-specific parameters and requirements.

