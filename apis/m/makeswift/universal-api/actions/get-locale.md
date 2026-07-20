# Makeswift: Get Locale

Retrieves a locale from Makeswift.

```
GET https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/get-locale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeswift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/get-locale?connectionId=$CONNECTION_ID&localeIdOrCode=string&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "localeIdOrCode": "string",
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/get-locale?${params}`, {
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
| `localeIdOrCode` | string | yes | Locale ID or locale code. |
| `siteId` | string | yes | The site ID containing the locale. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "id": "string",
      "isDefault": true,
      "locale": "string",
      "object": "string",
      "pathPrefix": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `id` | string |  |
| `isDefault` | boolean |  |
| `locale` | string |  |
| `object` | string |  |
| `pathPrefix` | string |  |

## Native endpoint

Through the native Makeswift API, this operation is `GET /v2/locales/:localeIdOrCode` (base URL `https://api.makeswift.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-locale.md) for the provider-specific parameters and requirements.

