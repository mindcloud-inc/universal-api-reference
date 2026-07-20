# Netlify: List Sites



```
GET https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-sites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-sites?${params}`, {
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
| `name` | string | no | Example: `testappsmindcloud`. |
| `filter` | list<string> | no | One of: `all`, `guest`, `owner`. |

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

Through the native Netlify API, this operation is `GET /sites` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sites.md) for the provider-specific parameters and requirements.

