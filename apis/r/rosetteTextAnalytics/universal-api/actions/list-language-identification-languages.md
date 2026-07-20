# Rosette Text Analytics: List Language Identification Languages



```
GET https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/list-language-identification-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rosette Text Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/list-language-identification-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/list-language-identification-languages?${params}`, {
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
      "supportedLanguages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `supportedLanguages` | array<object> |  |

## Native endpoint

Through the native Rosette Text Analytics API, this operation is `GET /language/supported-languages` (base URL `https://api.rosette.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-language-identification-languages.md) for the provider-specific parameters and requirements.

