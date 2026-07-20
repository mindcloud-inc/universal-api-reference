# Automate Team - Task Management: Lookup Workspace



```
GET https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/lookup-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Automate Team - Task Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/lookup-workspace?connectionId=$CONNECTION_ID&apiKeyFilter=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apiKeyFilter": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/lookup-workspace?${params}`, {
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
| `apiKeyFilter` | string | yes | PostgREST filter for the tenant API key, for example eq.<api-key>. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "status": true,
      "workspace_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `status` | boolean |  |
| `workspace_id` | number |  |

## Native endpoint

Through the native Automate Team - Task Management API, this operation is `GET /rest/v1/api_key` (base URL `https://api.automatebusiness.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-workspace.md) for the provider-specific parameters and requirements.

