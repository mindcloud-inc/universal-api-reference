# One-Time Secret: Get Supported Locales

Retrieves supported locales from One-Time Secret.

```
GET https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-get-supported-locales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a One-Time Secret `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-get-supported-locales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-get-supported-locales?${params}`, {
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
      "default_locale": "string",
      "locale": "string",
      "locales": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default_locale` | string | Default locale identifier. |
| `locale` | string | Locale used for the response. |
| `locales` | array<string> | Supported locale identifiers. |
| `success` | boolean | Whether the locale request succeeded. |

## Native endpoint

Through the native One-Time Secret API, this operation is `GET /api/v2/supported-locales` (base URL `https://us.onetimesecret.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-get-supported-locales.md) for the provider-specific parameters and requirements.

