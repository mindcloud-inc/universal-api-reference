# Netlify: Create Site Build Hook



```
POST https://connect.mindcloud.co/v1/universal/netlify/latest/actions/create-site-build-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/create-site-build-hook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netlify/latest/actions/create-site-build-hook', {
  method: 'POST',
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
| `siteId` | list<string> | yes |  |
| `title` | string | no | Example: `Main branch build hook`. |
| `branch` | string | no | Example: `main`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "draft": true,
      "id": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch` | string | Target branch |
| `createdAt` | date | Creation timestamp |
| `draft` | boolean | Whether draft deploys are enabled |
| `id` | string | Build hook ID |
| `title` | string | Build hook title |
| `url` | string | Build hook URL |

## Native endpoint

Through the native Netlify API, this operation is `POST /sites/:site_id/build_hooks` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site-build-hook.md) for the provider-specific parameters and requirements.

