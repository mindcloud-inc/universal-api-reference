# Supabugs: Get Project

Retrieves current project details from Supabugs.

```
GET https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabugs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/get-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/get-project?${params}`, {
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
      "archived": true,
      "clientCompanyName": "Ava Chen",
      "closedIssuesCount": 1,
      "code": "string",
      "contractNumber": "string",
      "description": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "issuesCount": 1,
      "name": "Ava Chen",
      "openIssuesCount": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `clientCompanyName` | string |  |
| `closedIssuesCount` | number |  |
| `code` | string |  |
| `contractNumber` | string |  |
| `description` | string |  |
| `endDate` | date |  |
| `id` | string |  |
| `issuesCount` | number |  |
| `name` | string |  |
| `openIssuesCount` | number |  |
| `startDate` | date |  |
| `status` | string |  |

## Native endpoint

Through the native Supabugs API, this operation is `GET /project` (base URL `https://api.supabugs.io/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

