# Sifter: List Project People

Retrieves assigned people for a project from Sifter.

```
GET https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-project-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sifter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-project-people?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-project-people?${params}`, {
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
      "apiIssuesUrl": "https://example.com",
      "email": "ava@example.com",
      "firstName": "Ava",
      "issuesUrl": "https://example.com",
      "lastName": "Chen",
      "name": "Ava Chen",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiIssuesUrl` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `issuesUrl` | string |  |
| `lastName` | string |  |
| `name` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Sifter API, this operation is `GET /projects/:project_id/people` (base URL `https://{{credentials.subdomain}}.sifterapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-people.md) for the provider-specific parameters and requirements.

