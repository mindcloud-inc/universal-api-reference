# Sifter: List Project Milestones

Retrieves milestones for a project from Sifter.

```
GET https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-project-milestones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sifter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-project-milestones?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-project-milestones?${params}`, {
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
| `projectId` | number | yes | The Sifter project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "apiIssuesUrl": "https://example.com",
      "dueDate": "string",
      "issuesUrl": "https://example.com",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `apiIssuesUrl` | string |  |
| `dueDate` | string |  |
| `issuesUrl` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Sifter API, this operation is `GET /projects/:project_id/milestones` (base URL `https://{{credentials.subdomain}}.sifterapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-milestones.md) for the provider-specific parameters and requirements.

