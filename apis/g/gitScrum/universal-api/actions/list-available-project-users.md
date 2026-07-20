# GitScrum: List Available Project Users

Retrieves available users for a GitScrum project.

```
GET https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/list-available-project-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitScrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/list-available-project-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/list-available-project-users?${params}`, {
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
| `companySlug` | string | no |  |
| `projectSlug` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native GitScrum API, this operation is `GET /project-members/:projectSlug/available-users` (base URL `https://services.gitscrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-project-users.md) for the provider-specific parameters and requirements.

