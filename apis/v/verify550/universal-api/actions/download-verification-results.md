# Verify550: Download Verification Results

Downloads verification result files from Verify550.

```
GET https://connect.mindcloud.co/v1/universal/verify550/latest/actions/download-verification-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verify550 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verify550/latest/actions/download-verification-results?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verify550/latest/actions/download-verification-results?${params}`, {
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
| `jobId` | string | yes | Verify550 bulk verification job ID. |
| `categories[]` | array<string> | no | Optional result categories to include in the export. Accepts multiple values in one string, delimited by `,`. |
| `format` | string | no | Export file format. One of: `csv`, `xlsx`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Verify550 API returns.

## Native endpoint

Through the native Verify550 API, this operation is `GET /jobexport/:jobId` (base URL `https://app.verify550.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-verification-results.md) for the provider-specific parameters and requirements.

