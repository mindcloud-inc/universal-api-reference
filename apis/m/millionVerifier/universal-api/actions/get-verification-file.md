# MillionVerifier: Get Verification File

Retrieves a verification file from MillionVerifier.

```
GET https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/get-verification-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MillionVerifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/get-verification-file?connectionId=$CONNECTION_ID&fileId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/get-verification-file?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "catchAll": 1,
      "createdate": "string",
      "credit": 1,
      "disposable": 1,
      "error": "string",
      "estimatedTimeSec": 1,
      "fileId": "string",
      "fileName": "Ava Chen",
      "invalid": 1,
      "ok": 1,
      "percent": 1,
      "reverify": 1,
      "status": "string",
      "totalRows": 1,
      "uniqueEmails": 1,
      "unknown": 1,
      "unverified": 1,
      "updatedAt": "string",
      "verified": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `catchAll` | number |  |
| `createdate` | string |  |
| `credit` | number |  |
| `disposable` | number |  |
| `error` | string |  |
| `estimatedTimeSec` | number |  |
| `fileId` | string |  |
| `fileName` | string |  |
| `invalid` | number |  |
| `ok` | number |  |
| `percent` | number |  |
| `reverify` | number |  |
| `status` | string |  |
| `totalRows` | number |  |
| `uniqueEmails` | number |  |
| `unknown` | number |  |
| `unverified` | number |  |
| `updatedAt` | string |  |
| `verified` | number |  |

## Native endpoint

Through the native MillionVerifier API, this operation is `GET https://bulkapi.millionverifier.com/bulkapi/v2/fileinfo` (base URL `https://api.millionverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-verification-file.md) for the provider-specific parameters and requirements.

