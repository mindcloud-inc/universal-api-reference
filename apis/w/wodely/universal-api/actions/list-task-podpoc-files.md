# Wodely: List Task POD/POC Files



```
GET https://connect.mindcloud.co/v1/universal/wodely/latest/actions/list-task-podpoc-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/list-task-podpoc-files?connectionId=$CONNECTION_ID&taskGuid=your-task-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskGuid": "your-task-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wodely/latest/actions/list-task-podpoc-files?${params}`, {
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
| `taskGuid` | string | yes | Task identifier returned by Wodely. Example: `your-task-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "createdDateTime": "string",
      "createdUserId": "string",
      "data": "string",
      "fileDesc": "string",
      "fileGuid": "string",
      "fileName": "Ava Chen",
      "id": 1,
      "taskId": 1,
      "typeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | File MIME content type. |
| `createdDateTime` | string | File creation timestamp in UTC. |
| `createdUserId` | string | User identifier that created the file. |
| `data` | string | Encoded file data returned by Wodely. |
| `fileDesc` | string | File description. |
| `fileGuid` | string | File GUID. |
| `fileName` | string | File name. |
| `id` | number | File identifier. |
| `taskId` | number | Numeric task identifier linked to the file. |
| `typeId` | number | Wodely file type identifier. |

## Native endpoint

Through the native Wodely API, this operation is `GET /v2/taskFiles/[:taskGuid]` (base URL `https://api.wodely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-podpoc-files.md) for the provider-specific parameters and requirements.

