# Makeswift: Duplicate Site

Creates a copy of a site in Makeswift.

```
POST https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/duplicate-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeswift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/duplicate-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/duplicate-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | yes | The source site ID to duplicate. |
| `name` | string | yes | Name for the duplicated site. |

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

Through the native Makeswift API, this operation is `POST /v2/sites/:siteId/duplicate` (base URL `https://api.makeswift.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-site.md) for the provider-specific parameters and requirements.

