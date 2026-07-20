# What3Words: List Available what3words Languages

Lists available what3words languages for 3 word addresses.

```
GET https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/list-available-what3words-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a What3Words `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/list-available-what3words-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/list-available-what3words-languages?${params}`, {
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
      "locales": [
        {}
      ],
      "name": "Ava Chen",
      "nativeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | what3words language or locale code. |
| `locales` | array<object> | Available locale variants for the language, when applicable. |
| `name` | string | English language name. |
| `nativeName` | string | Language name in its native script. |

## Native endpoint

Through the native What3Words API, this operation is `GET /available-languages` (base URL `https://api.what3words.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-what3words-languages.md) for the provider-specific parameters and requirements.

