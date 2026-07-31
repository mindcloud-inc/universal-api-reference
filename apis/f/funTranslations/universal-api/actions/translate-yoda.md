# Fun Translations: Translate to Yoda



```
GET https://connect.mindcloud.co/v1/universal/funTranslations/latest/actions/translate-yoda
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fun Translations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/funTranslations/latest/actions/translate-yoda?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/funTranslations/latest/actions/translate-yoda?${params}`, {
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
| `text` | string | yes | Required text to translate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contents": {},
      "success": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contents` | object |  |
| `success` | object |  |

## Native endpoint

Through the native Fun Translations API, this operation is `POST /yodish` (base URL `https://api.funtranslations.com/translate`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/translate-yoda.md) for the provider-specific parameters and requirements.

