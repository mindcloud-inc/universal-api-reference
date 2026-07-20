# Sifter: List All Projects

Retrieves all accessible projects from Sifter.

```
GET https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-all-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sifter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-all-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-all-projects?${params}`, {
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

Through the native Sifter API, this operation is `GET /projects` (base URL `https://{{credentials.subdomain}}.sifterapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-projects.md) for the provider-specific parameters and requirements.

