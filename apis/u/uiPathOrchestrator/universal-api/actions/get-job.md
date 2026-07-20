# UiPath Orchestrator: Get job



```
GET https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UiPath Orchestrator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-job?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-job?${params}`, {
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
| `id` | number | yes | The numeric job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreationTime": "2026-05-07T12:00:00.000Z",
      "EndTime": "2026-05-07T12:00:00.000Z",
      "Id": 1,
      "Info": "string",
      "Key": "string",
      "Source": "string",
      "StartTime": "2026-05-07T12:00:00.000Z",
      "State": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreationTime` | date |  |
| `EndTime` | date |  |
| `Id` | number |  |
| `Info` | string |  |
| `Key` | string |  |
| `Source` | string |  |
| `StartTime` | date |  |
| `State` | string |  |

## Native endpoint

Through the native UiPath Orchestrator API, this operation is `GET /odata/Jobs(:id)` (base URL `https://cloud.uipath.com/{{credentials.organizationName}}/{{credentials.tenantName}}/orchestrator_`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

