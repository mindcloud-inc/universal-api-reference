# GitScrum: List Workspaces

Retrieves a list of GitScrum workspaces.

```
GET https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitScrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/list-workspaces?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "favicon": "string",
      "header_color": "string",
      "is_only_workspace": true,
      "is_owner": true,
      "is_subscription_workspace": true,
      "logged_user_role": {},
      "logo": "string",
      "my_company_default": true,
      "name": "Ava Chen",
      "settings": {},
      "slug": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `favicon` | string |  |
| `header_color` | string |  |
| `is_only_workspace` | boolean |  |
| `is_owner` | boolean |  |
| `is_subscription_workspace` | boolean |  |
| `logged_user_role` | object |  |
| `logo` | string |  |
| `my_company_default` | boolean |  |
| `name` | string |  |
| `settings` | object |  |
| `slug` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native GitScrum API, this operation is `GET /companies` (base URL `https://services.gitscrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

