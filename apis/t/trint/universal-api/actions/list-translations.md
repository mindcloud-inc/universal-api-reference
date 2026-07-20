# Trint: List Translations

Retrieves translations from your Trint account.

```
GET https://connect.mindcloud.co/v1/universal/trint/latest/actions/list-translations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trint/latest/actions/list-translations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trint/latest/actions/list-translations?${params}`, {
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
      "source": {},
      "translations": [
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
| `source` | object | Source transcript translation reference. |
| `translations` | array<object> | Translated transcript references linked to the source file. |

## Native endpoint

Through the native Trint API, this operation is `GET https://translation.api.trint.com/` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-translations.md) for the provider-specific parameters and requirements.

