# Amberscript: Export VTT

Retrieves VTT subtitle export for an Amberscript job.

```
GET https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/export-vtt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amberscript `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/export-vtt?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/export-vtt?${params}`, {
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
| `jobId` | string | yes | The finished job to export. |
| `maxCharsPerRow` | number | no | Maximum characters per subtitle row. Default: `42`. |
| `maxNumberOfRows` | number | no | Maximum number of subtitle rows per caption. Default: `2`. |
| `maxScreenTimePerRowSeconds` | number | no | Maximum number of seconds allocated to each subtitle row. Default: `2`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amberscript API returns.

## Native endpoint

Through the native Amberscript API, this operation is `GET /jobs/export-vtt` (base URL `https://api.amberscript.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-vtt.md) for the provider-specific parameters and requirements.

