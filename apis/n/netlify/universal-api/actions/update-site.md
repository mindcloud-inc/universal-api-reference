# Netlify: Update Site



```
PUT https://connect.mindcloud.co/v1/universal/netlify/latest/actions/update-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/update-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string",
  "name": "mc-stage3-example-updated"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netlify/latest/actions/update-site', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string",
    "name": "mc-stage3-example-updated"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | list<string> | yes | The Netlify site ID. |
| `name` | string | yes | The site name. Example: `mc-stage3-example-updated`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminUrl": "https://example.com",
      "claimed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultDomain": "string",
      "deployUrl": "https://example.com",
      "id": "string",
      "managedDns": true,
      "name": "Ava Chen",
      "plan": "string",
      "siteId": "string",
      "ssl": true,
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminUrl` | string |  |
| `claimed` | boolean |  |
| `createdAt` | date |  |
| `defaultDomain` | string |  |
| `deployUrl` | string |  |
| `id` | string |  |
| `managedDns` | boolean |  |
| `name` | string |  |
| `plan` | string |  |
| `siteId` | string |  |
| `ssl` | boolean |  |
| `state` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Netlify API, this operation is `PATCH /sites/:site_id` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-site.md) for the provider-specific parameters and requirements.

