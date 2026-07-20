# Sifter: Get Project Metadata

Retrieves detailed project metadata from Sifter.

```
GET https://connect.mindcloud.co/v1/universal/sifter/latest/actions/get-project-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sifter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sifter/latest/actions/get-project-metadata?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sifter/latest/actions/get-project-metadata?${params}`, {
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
| `projectId` | number | yes |  |

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
      "categories": [
        {}
      ],
      "issuesUrl": "https://example.com",
      "milestones": [
        {}
      ],
      "milestonesUrl": "https://example.com",
      "name": "Ava Chen",
      "people": [
        {}
      ],
      "primaryCompanyName": "Ava Chen",
      "priorities": [
        {}
      ],
      "statuses": [
        {}
      ],
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
| `categories` | array<object> |  |
| `issuesUrl` | string |  |
| `milestones` | array<object> |  |
| `milestonesUrl` | string |  |
| `name` | string |  |
| `people` | array<object> |  |
| `primaryCompanyName` | string |  |
| `priorities` | array<object> |  |
| `statuses` | array<object> |  |
| `url` | string |  |

## Native endpoint

Through the native Sifter API, this operation is `GET /projects/:project_id` (base URL `https://{{credentials.subdomain}}.sifterapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-metadata.md) for the provider-specific parameters and requirements.

