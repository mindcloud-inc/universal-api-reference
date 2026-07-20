# Pipedream Utils: Formatting - [Date/Time] Add/Subtract Time

Adds or subtracts time from a date in Pipedream Utils.

```
GET https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/add-subtract-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/add-subtract-time?connectionId=$CONNECTION_ID&inputDate=string&operation=string&duration=string&outputFormat=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputDate": "string",
  "operation": "string",
  "duration": "string",
  "outputFormat": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/add-subtract-time?${params}`, {
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
| `inputDate` | string | yes | A valid date string, in the format selected in Input Format. |
| `inputFormat` | string | no | The format of the input date string. If omitted, the parser will try to infer it. |
| `operation` | string | yes | Whether to add or subtract time. |
| `duration` | string | yes | The duration for the operation. You can use the shorthand duration, for example: `1s`, `1m`, `1h`, `1d`, `1w`, `1y` equal one second, minute, hour, day, week, and year respectively |
| `outputFormat` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pipedream Utils API returns.

## Native endpoint

Through the native Pipedream Utils API, this operation is `GET` (base URL `https://pipedream.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subtract-time.md) for the provider-specific parameters and requirements.

