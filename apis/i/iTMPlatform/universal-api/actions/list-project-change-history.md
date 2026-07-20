# ITM Platform: List Project Change History



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-project-change-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-project-change-history?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-project-change-history?${params}`, {
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
| `projectId` | string | yes | The ITM Platform project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "budgetAccounts": [
        1
      ],
      "documents": [
        1
      ],
      "progressReports": [
        1
      ],
      "projectGeneral": [
        1
      ],
      "revenue": [
        1
      ],
      "risks": [
        1
      ],
      "tasks": [
        1
      ],
      "users": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `budgetAccounts` | array<number> |  |
| `documents` | array<number> |  |
| `progressReports` | array<number> |  |
| `projectGeneral` | array<number> |  |
| `revenue` | array<number> |  |
| `risks` | array<number> |  |
| `tasks` | array<number> |  |
| `users` | array<number> |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /Projects/{ProjectId}/changeHistory` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-change-history.md) for the provider-specific parameters and requirements.

