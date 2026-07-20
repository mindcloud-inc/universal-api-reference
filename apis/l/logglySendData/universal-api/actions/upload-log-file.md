# Loggly (Send Data): Upload Log File

Uploads a log file to Loggly.

```
POST https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/upload-log-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loggly (Send Data) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/upload-log-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerToken": "123e4567-e89b-12d3-a456-426614174000",
  "tagPath": "file_upload",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/upload-log-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerToken": "123e4567-e89b-12d3-a456-426614174000",
    "tagPath": "file_upload",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerToken` | string | yes | Example: `123e4567-e89b-12d3-a456-426614174000`. |
| `tagPath` | string | yes | Example: `file_upload`. |
| `file` | file | yes | Text log file to upload. Each line becomes an event in Loggly. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Loggly ingestion acknowledgement message. |

## Native endpoint

Through the native Loggly (Send Data) API, this operation is `POST /bulk/:customerToken/tag/:tagPath/` (base URL `https://logs-01.loggly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-log-file.md) for the provider-specific parameters and requirements.

