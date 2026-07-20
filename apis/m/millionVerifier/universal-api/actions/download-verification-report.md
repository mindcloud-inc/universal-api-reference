# MillionVerifier: Download Verification Report

Downloads a verification report from MillionVerifier.

```
GET https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/download-verification-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MillionVerifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/download-verification-report?connectionId=$CONNECTION_ID&fileId=1&filter=all" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "1",
  "filter": "all"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/download-verification-report?${params}`, {
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
| `fileId` | number | yes | The ID of the uploaded file. |
| `filter` | string | yes | Report filter preset. Default: `all`. Example: `all`. |
| `statuses` | string | no | Comma-separated statuses to include when filter is custom. Example: `ok,invalid`. |
| `free` | string | no | Whether to include only free or non-free domains when filter is custom. Example: `1`. |
| `role` | string | no | Whether to include only role or non-role emails when filter is custom. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | number |  |
| `type` | string |  |

## Native endpoint

Through the native MillionVerifier API, this operation is `GET https://bulkapi.millionverifier.com/bulkapi/v2/download` (base URL `https://api.millionverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-verification-report.md) for the provider-specific parameters and requirements.

