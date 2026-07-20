# Makeswift: Update Locale

Updates an existing locale in Makeswift.

```
PUT https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/update-locale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeswift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/update-locale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "localeIdOrCode": "string",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/update-locale', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "localeIdOrCode": "string",
    "siteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `localeIdOrCode` | string | yes | Locale ID or locale code to update. |
| `siteId` | string | yes | The site ID containing the locale. |
| `locale` | string | no | Updated locale code. |
| `domain` | string | no | Custom domain for this locale. |
| `pathPrefix` | string | no | Path prefix for this locale, e.g. /fr. |

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
      "object": "string"
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

## Native endpoint

Through the native Makeswift API, this operation is `PATCH /v2/locales/:localeIdOrCode` (base URL `https://api.makeswift.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-locale.md) for the provider-specific parameters and requirements.

