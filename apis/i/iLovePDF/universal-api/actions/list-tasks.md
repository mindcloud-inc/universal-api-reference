# iLovePDF: List Tasks

Retrieves tasks from iLovePDF.

```
GET https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/list-tasks?${params}`, {
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
| `page` | number | no | Task results page number. iLovePDF returns 50 results per page. Default: `1`. |
| `tool` | string | no | Filter tasks by iLovePDF tool key such as merge or compress. |
| `status` | string | no | Filter tasks by task status such as TaskSuccess. |
| `customInt` | number | no | Filter tasks by the custom integer metadata value stored on the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_int": 1,
      "custom_string": "string",
      "download_filename": "Ava Chen",
      "file_number": "string",
      "filesize": 1,
      "output_extensions": [
        "string"
      ],
      "output_filenumber": 1,
      "output_filesize": 1,
      "process_start": "string",
      "server": "string",
      "status": "string",
      "status_message": "string",
      "task": "string",
      "timer": "string",
      "tool": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_int` | number |  |
| `custom_string` | string |  |
| `download_filename` | string |  |
| `file_number` | string |  |
| `filesize` | number |  |
| `output_extensions[]` | string |  |
| `output_filenumber` | number |  |
| `output_filesize` | number |  |
| `process_start` | string |  |
| `server` | string |  |
| `status` | string |  |
| `status_message` | string |  |
| `task` | string |  |
| `timer` | string |  |
| `tool` | string |  |

## Native endpoint

Through the native iLovePDF API, this operation is `POST /task` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

