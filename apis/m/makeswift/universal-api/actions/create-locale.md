# Makeswift: Create Locale

Creates a new locale for a site in Makeswift.

```
POST https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/create-locale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeswift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/create-locale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string",
  "locale": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/create-locale', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string",
    "locale": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | yes | Site ID where the locale will be created. |
| `locale` | string | yes | Locale code (for example en-US). |

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

Through the native Makeswift API, this operation is `POST /v2/locales` (base URL `https://api.makeswift.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-locale.md) for the provider-specific parameters and requirements.

