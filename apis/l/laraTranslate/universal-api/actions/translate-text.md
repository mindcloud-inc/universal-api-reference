# Lara Translate: Translate text

Translates text from one language to another in Lara Translate.

```
GET https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/translate-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lara Translate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/translate-text?connectionId=$CONNECTION_ID&text%5B%5D=%5Bobject%20Object%5D&target=it-IT" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text[]": "[object Object]",
  "target": "it-IT"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/translate-text?${params}`, {
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
| `text[]` | array<object> | yes | Array of text blocks to translate. Each item should include text and a translatable boolean. |
| `source` | string | no | Optional source language code such as en-US. Example: `en-US`. |
| `target` | string | yes | Target language code such as it-IT. Example: `it-IT`. |
| `context` | string | no | Optional context to improve translation quality. |
| `instructions[]` | array<string> | no | Optional list of short localization directives. |
| `source_hint` | string | no | Optional language hint to guide detection. Example: `en-US`. |
| `adapt_to[]` | array<string> | no | Optional list of translation memory IDs to adapt to. |
| `style` | list | no | Optional translation style. One of: `Creative`, `Faithful`, `Fluid`. |
| `reasoning` | boolean | no | Whether to include reasoning in the translation response. |
| `content_type` | list | no | Content type of the source text. One of: `HTML`, `Plain text`, `XLIFF`. |
| `no_trace` | boolean | no | If true, Lara does not store the translation in logs. |
| `priority` | list | no | Optional translation request priority. One of: `Background`, `Normal`. |
| `timeout_in_millis` | number | no | Custom timeout for the translation request in milliseconds. Maximum 300000. Example: `2000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "text": "string",
      "translatable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `text` | string | Translated text block. |
| `translatable` | boolean | Whether the block is translatable. |

## Native endpoint

Through the native Lara Translate API, this operation is `POST /` (base URL `https://mcp-v2.laratranslate.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/translate-text.md) for the provider-specific parameters and requirements.

