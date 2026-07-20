# LaunchNotes: Search Project



```
GET https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/search-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/search-project?connectionId=$CONNECTION_ID&projectId=string&searchTerm=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "searchTerm": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/search-project?${params}`, {
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
| `projectId` | string | yes | Project to search. |
| `searchTerm` | string | yes | Search term to match inside the project. |
| `limit` | number | no | Optional maximum number of results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__typename": "Ava Chen",
      "content": "string",
      "email": "ava@example.com",
      "feedbackCount": 1,
      "headline": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__typename` | string | Search result object type. |
| `content` | string | Work item content when the result is a work item. |
| `email` | string | Subscriber email when the result is a subscriber. |
| `feedbackCount` | number | Feedback count when the result is an idea. |
| `headline` | string | Announcement headline when the result is an announcement. |
| `id` | string | Search result identifier. |

## Native endpoint

Through the native LaunchNotes API, this operation is `POST /graphql` (base URL `https://app.launchnotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-project.md) for the provider-specific parameters and requirements.

