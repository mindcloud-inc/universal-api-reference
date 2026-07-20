# Appwrite: Get log

Retrieves the log from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/sites-get-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/sites-get-log?connectionId=$CONNECTION_ID&siteId=string&logId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string",
  "logId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/sites-get-log?${params}`, {
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
| `siteId` | string | yes | Site ID. |
| `logId` | string | yes | Log ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$permissions": [
        "string"
      ],
      "$updatedAt": "string",
      "deploymentId": "string",
      "duration": 1,
      "errors": "string",
      "functionId": "string",
      "logs": "string",
      "requestHeaders": [
        {}
      ],
      "requestMethod": "string",
      "requestPath": "string",
      "responseBody": "string",
      "responseHeaders": [
        {}
      ],
      "responseStatusCode": 1,
      "scheduledAt": "string",
      "status": "string",
      "trigger": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Execution creation date in ISO 8601 format. |
| `$id` | string | Execution ID. |
| `$permissions` | array<string> | Execution roles. |
| `$updatedAt` | string | Execution update date in ISO 8601 format. |
| `deploymentId` | string | Function's deployment ID used to create the execution. |
| `duration` | number | Resource(function/site) execution duration in seconds. |
| `errors` | string | Function errors. Includes the last 4,000 characters. This will return an empty string unless the response is returned using an API key or as part of a webhook payload. |
| `functionId` | string | Function ID. |
| `logs` | string | Function logs. Includes the last 4,000 characters. This will return an empty string unless the response is returned using an API key or as part of a webhook payload. |
| `requestHeaders` | array<object> | HTTP request headers as a key-value object. This will return only whitelisted headers. All headers are returned if execution is created as synchronous. |
| `requestMethod` | string | HTTP request method type. |
| `requestPath` | string | HTTP request path and query. |
| `responseBody` | string | HTTP response body. This will return empty unless execution is created as synchronous. |
| `responseHeaders` | array<object> | HTTP response headers as a key-value object. This will return only whitelisted headers. All headers are returned if execution is created as synchronous. |
| `responseStatusCode` | number | HTTP response status code. |
| `scheduledAt` | string | The scheduled time for execution. If left empty, execution will be queued immediately. |
| `status` | string | The status of the function execution. Possible values can be: `waiting`, `processing`, `completed`, `failed`, or `scheduled`. |
| `trigger` | string | The trigger that caused the function to execute. Possible values can be: `http`, `schedule`, or `event`. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /sites/{siteId}/logs/{logId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sites-get-log.md) for the provider-specific parameters and requirements.

