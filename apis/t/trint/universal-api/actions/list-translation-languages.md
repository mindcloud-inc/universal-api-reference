# Trint: List Translation Languages

Retrieves translation languages from Trint.

```
GET https://connect.mindcloud.co/v1/universal/trint/latest/actions/list-translation-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trint/latest/actions/list-translation-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trint/latest/actions/list-translation-languages?${params}`, {
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
      "data": {
        "translationLanguages": [
          {
            "languageCode": "string",
            "languageName": "Ava Chen"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.translationLanguages` | array<object> | Supported translation languages. |
| `data.translationLanguages[].languageCode` | string | Language code accepted by the translation API. |
| `data.translationLanguages[].languageName` | string | Display name of the translation language. |

## Native endpoint

Through the native Trint API, this operation is `GET https://translation.api.trint.com/translation-languages` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-translation-languages.md) for the provider-specific parameters and requirements.

