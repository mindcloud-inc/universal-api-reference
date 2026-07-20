# Tisane Labs: List Languages

Retrieves supported languages from Tisane Labs.

```
GET https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/list-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tisane Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/list-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/list-languages?${params}`, {
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
      "encoding": "string",
      "englishName": "Ava Chen",
      "fontFace": "string",
      "isLatinScript": true,
      "isoCode": "string",
      "loaded": true,
      "name": "Ava Chen",
      "rightToLeft": true,
      "segmentation": "string",
      "systemLanguage": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `encoding` | string | Language encoding. |
| `englishName` | string | English language name. |
| `fontFace` | string | Recommended font for display. |
| `isLatinScript` | boolean | Whether the language uses Latin script. |
| `isoCode` | string | Language ISO code. |
| `loaded` | boolean | Whether the language resources are loaded. |
| `name` | string | Native language name. |
| `rightToLeft` | boolean | Whether the language uses right-to-left script. |
| `segmentation` | string | Segmentation mode used for the language. |
| `systemLanguage` | boolean | Whether this is a system language. |

## Native endpoint

Through the native Tisane Labs API, this operation is `GET /languages` (base URL `https://api.tisane.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-languages.md) for the provider-specific parameters and requirements.

