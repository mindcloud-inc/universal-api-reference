# ClickUp: List Task Templates



```
GET https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-task-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-task-templates?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-task-templates?${params}`, {
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
| `teamId` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "templates": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `templates` | array |  |
| `templates[]` | string |  |

## Native endpoint

Through the native ClickUp API, this operation is `GET team/:team_id/taskTemplate` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-templates.md) for the provider-specific parameters and requirements.

