# Sifter: Get Project

Retrieves a specific project from Sifter.

```
GET https://connect.mindcloud.co/v1/universal/sifter/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sifter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sifter/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sifter/latest/actions/get-project?${params}`, {
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
      "apiCategoriesUrl": "https://example.com",
      "apiIssuesUrl": "https://example.com",
      "apiMilestonesUrl": "https://example.com",
      "apiNewIssueEmailAddress": "ava@example.com",
      "apiPeopleUrl": "https://example.com",
      "apiUrl": "https://example.com",
      "archived": true,
      "issuesUrl": "https://example.com",
      "milestonesUrl": "https://example.com",
      "name": "Ava Chen",
      "primaryCompanyName": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiCategoriesUrl` | string |  |
| `apiIssuesUrl` | string |  |
| `apiMilestonesUrl` | string |  |
| `apiNewIssueEmailAddress` | string |  |
| `apiPeopleUrl` | string |  |
| `apiUrl` | string |  |
| `archived` | boolean |  |
| `issuesUrl` | string |  |
| `milestonesUrl` | string |  |
| `name` | string |  |
| `primaryCompanyName` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Sifter API, this operation is `GET /projects/:project_id` (base URL `https://{{credentials.subdomain}}.sifterapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

