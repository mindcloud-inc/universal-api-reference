# WebSpellChecker: Get Info

Retrieves subscription details from WebSpellChecker.

```
GET https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/get-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebSpellChecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/get-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/get-info?${params}`, {
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
      "banner": true,
      "canRemoveBranding": true,
      "cdModificationTime": 1,
      "freeze": 1,
      "generateLangList": {},
      "grammarLangList": {},
      "langList": {},
      "maxGenerateInputSize": 1,
      "minGenerateInputSize": 1,
      "programVersion": "string",
      "prompts": {},
      "sendStatistics": true,
      "session": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `banner` | boolean | Branding/banner flag. |
| `canRemoveBranding` | boolean | Whether branding removal is allowed. |
| `cdModificationTime` | number | Dictionary data modification timestamp. |
| `freeze` | number | Service freeze indicator. |
| `generateLangList` | object | Available generation languages. |
| `grammarLangList` | object | Available grammar languages grouped by text direction. |
| `langList` | object | Available spelling languages grouped by text direction. |
| `maxGenerateInputSize` | number | Maximum supported input size for text generation prompts. |
| `minGenerateInputSize` | number | Minimum supported input size for text generation prompts. |
| `programVersion` | string | Provider version string. |
| `prompts` | object | Available prompt labels for generation helpers. |
| `sendStatistics` | boolean | Whether service statistics sending is enabled. |
| `session` | string | Session identifier returned by the API. |

## Native endpoint

Through the native WebSpellChecker API, this operation is `GET /` (base URL `https://svc.webspellchecker.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-info.md) for the provider-specific parameters and requirements.

