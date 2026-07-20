# Firebolt: Check Async Query Status

Retrieves asynchronous query status from Firebolt.

```
GET https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/check-async-query-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/check-async-query-status?connectionId=$CONNECTION_ID&engineUrl=01abcde12345.api.us-east-1.app.firebolt.io&asyncToken=CiQ..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "engineUrl": "01abcde12345.api.us-east-1.app.firebolt.io",
  "asyncToken": "CiQ..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/check-async-query-status?${params}`, {
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
| `engineUrl` | string | yes | Firebolt engine URL host or engine endpoint used to check async query status. Example: `01abcde12345.api.us-east-1.app.firebolt.io`. |
| `asyncToken` | string | yes | Async query token returned by Firebolt. Example: `CiQ...`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `database` | string | no | Database to target for user-engine async status checks when required. Example: `analytics`. |
| `engineName` | string | no | User engine name to target when checking async query status on a user engine. Example: `mc_fb_act_20260422_engine`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountName": "Ava Chen",
      "endTime": "string",
      "errorMessage": "string",
      "queryId": "string",
      "requestId": "string",
      "retries": "string",
      "scannedBytes": "string",
      "scannedRows": "string",
      "startTime": "string",
      "status": "string",
      "submittedTime": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountName` | string |  |
| `endTime` | string |  |
| `errorMessage` | string |  |
| `queryId` | string |  |
| `requestId` | string |  |
| `retries` | string |  |
| `scannedBytes` | string |  |
| `scannedRows` | string |  |
| `startTime` | string |  |
| `status` | string |  |
| `submittedTime` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineUrl` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-async-query-status.md) for the provider-specific parameters and requirements.

