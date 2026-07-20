# Appwrite: List languages

Retrieves a list of languages from Appwrite.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/locale-list-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/locale-list-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/locale-list-languages?${params}`, {
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
      "languages": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `languages` | array<object> | List of languages. |
| `total` | number | Total number of languages that matched your query. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /locale/languages` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/locale-list-languages.md) for the provider-specific parameters and requirements.

