# Clockify: List My Shared Reports

Lists your shared reports in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-my-shared-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-my-shared-reports?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-my-shared-reports?${params}`, {
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
| `page` | number | no |  |
| `pageSize` | number | no |  |
| `sharedReportsFilter` | list | no | One of: `ALL`, `CREATED_BY_ME`, `SHARED_WITH_ME`. |
| `workspaceId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "reports": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `reports[]` | array<object> |  |
| `reports[].fixedDate` | boolean |  |
| `reports[].id` | string |  |
| `reports[].isPublic` | boolean |  |
| `reports[].link` | string |  |
| `reports[].name` | string |  |
| `reports[].reportAuthor` | string |  |
| `reports[].type` | string |  |
| `reports[].visibleToUserGroups[]` | array<object> |  |
| `reports[].visibleToUserGroups[].id` | string |  |
| `reports[].visibleToUserGroups[].name` | string |  |
| `reports[].visibleToUsers[]` | array<object> |  |
| `reports[].visibleToUsers[].id` | string |  |
| `reports[].visibleToUsers[].name` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/shared-reports` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-my-shared-reports.md) for the provider-specific parameters and requirements.

