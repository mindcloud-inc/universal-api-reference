# Fidel API: Update Brand

Updates an existing brand in Fidel API.

```
PUT https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-brand" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "brandId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-brand', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "brandId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `brandId` | string | yes |  |
| `websiteURL` | string | no | URL for the Brand. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "consent": true,
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "live": true,
      "name": "Ava Chen",
      "updated": "2026-05-07T12:00:00.000Z",
      "websiteURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `consent` | boolean |  |
| `created` | date |  |
| `id` | string |  |
| `live` | boolean |  |
| `name` | string |  |
| `updated` | date |  |
| `websiteURL` | string |  |

## Native endpoint

Through the native Fidel API API, this operation is `PATCH /brands/:brandId` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-brand.md) for the provider-specific parameters and requirements.

