# Makeswift: Update Site

Updates an existing site in Makeswift.

```
PUT https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/update-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeswift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/update-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/update-site', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | yes | The site ID to update. |
| `name` | string | no | Updated name for the site. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultLocale": "string",
      "hostOrigin": "string",
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "publicApiKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultLocale` | string |  |
| `hostOrigin` | string |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `publicApiKey` | string |  |

## Native endpoint

Through the native Makeswift API, this operation is `PATCH /v2/sites/:siteId` (base URL `https://api.makeswift.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-site.md) for the provider-specific parameters and requirements.

