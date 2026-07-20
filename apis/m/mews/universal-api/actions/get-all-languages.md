# Mews: Get All Languages

Retrieves languages from Mews.

```
GET https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-languages?${params}`, {
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
      "code": "string",
      "englishName": "Ava Chen",
      "fallbackLanguageCode": "string",
      "localName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Language code. |
| `englishName` | string | English language name. |
| `fallbackLanguageCode` | string | Fallback language code when present. |
| `localName` | string | Localized language name. |

## Native endpoint

Through the native Mews API, this operation is `POST /languages/getAll` (base URL `{{credentials.platformAddress}}/api/connector/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-languages.md) for the provider-specific parameters and requirements.

