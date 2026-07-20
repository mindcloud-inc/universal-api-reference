# Florm: Get Export Task

Retrieves a specific Florm export task.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-export-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-export-task?connectionId=$CONNECTION_ID&formGuid=string&taskGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formGuid": "string",
  "taskGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-export-task?${params}`, {
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
| `formGuid` | string | yes | GUID of the Florm form tied to the export task. |
| `taskGuid` | string | yes | GUID of the Florm export task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resultString": "string",
      "status": "string",
      "taskGuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resultString` | string | Provider result string when available. |
| `status` | string | Current export task status. |
| `taskGuid` | string | GUID of the export task. |

## Native endpoint

Through the native Florm API, this operation is `GET /v1/export/form/:form_guid/task/:task_guid` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-export-task.md) for the provider-specific parameters and requirements.

