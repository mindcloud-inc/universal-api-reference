# ChangeCrab: Get Changelog

Retrieves a changelog from ChangeCrab.

```
GET https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/get-changelog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChangeCrab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/get-changelog?connectionId=$CONNECTION_ID&id=e.g.%20product-updates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "e.g. product-updates"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/get-changelog?${params}`, {
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
| `id` | string | yes | The ChangeCrab changelog access ID. Example: `e.g. product-updates`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accent": "string",
      "accessid": "string",
      "autonotify": true,
      "created_at": "string",
      "domain": "string",
      "id": 1,
      "name": "Ava Chen",
      "private": true,
      "showbrand": true,
      "showfilters": true,
      "siteurl": "https://example.com",
      "subdomain": "string",
      "subscribeactive": true,
      "suggestion": true,
      "team": 1,
      "team_name": "Ava Chen",
      "teamdetails": {},
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accent` | string |  |
| `accessid` | string |  |
| `autonotify` | boolean |  |
| `created_at` | string |  |
| `domain` | string |  |
| `id` | number |  |
| `name` | string |  |
| `private` | boolean |  |
| `showbrand` | boolean |  |
| `showfilters` | boolean |  |
| `siteurl` | string |  |
| `subdomain` | string |  |
| `subscribeactive` | boolean |  |
| `suggestion` | boolean |  |
| `team` | number |  |
| `team_name` | string |  |
| `teamdetails` | object |  |
| `updated_at` | string |  |

## Native endpoint

Through the native ChangeCrab API, this operation is `GET /changelogs/:id` (base URL `https://changecrab.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-changelog.md) for the provider-specific parameters and requirements.

