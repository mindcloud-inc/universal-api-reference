# UiPath Orchestrator: List tasks across folders



```
GET https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/list-tasks-across-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UiPath Orchestrator `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/list-tasks-across-folders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/list-tasks-across-folders?${params}`, {
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
      "CreationTime": "2026-05-07T12:00:00.000Z",
      "Id": 1,
      "Priority": "string",
      "Status": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreationTime` | date |  |
| `Id` | number |  |
| `Priority` | string |  |
| `Status` | string |  |
| `Title` | string |  |

## Native endpoint

Through the native UiPath Orchestrator API, this operation is `GET /odata/Tasks/UiPath.Server.Configuration.OData.GetTasksAcrossFolders` (base URL `https://cloud.uipath.com/{{credentials.organizationName}}/{{credentials.tenantName}}/orchestrator_`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks-across-folders.md) for the provider-specific parameters and requirements.

