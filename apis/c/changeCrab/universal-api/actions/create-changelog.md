# ChangeCrab: Create Changelog

Creates a new changelog in ChangeCrab.

```
POST https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/create-changelog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChangeCrab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/create-changelog" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "e.g. Product Updates",
  "team": "e.g. 101038"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/create-changelog', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "e.g. Product Updates",
    "team": "e.g. 101038"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The public name shown for the changelog. Example: `e.g. Product Updates`. |
| `team` | number | yes | The owning ChangeCrab team ID. Example: `e.g. 101038`. |
| `subdomain` | string | no | The changelog subdomain slug. Example: `e.g. product-updates`. |
| `siteurl` | string | no | The full website URL for the changelog. Example: `e.g. https://example.com/changelog`. |

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

Through the native ChangeCrab API, this operation is `POST /changelogs` (base URL `https://changecrab.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-changelog.md) for the provider-specific parameters and requirements.

