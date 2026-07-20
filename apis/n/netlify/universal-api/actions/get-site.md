# Netlify: Get Site



```
GET https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-site?connectionId=$CONNECTION_ID&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-site?${params}`, {
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
| `siteId` | list<string> | yes | The Netlify site ID. |

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

Through the native Netlify API, this operation is `GET /sites/:site_id` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

