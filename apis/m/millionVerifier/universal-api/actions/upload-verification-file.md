# MillionVerifier: Upload Verification File

Uploads a verification file to MillionVerifier.

```
POST https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/upload-verification-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MillionVerifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/upload-verification-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileContents": "/tmp/emails.csv"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/upload-verification-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileContents": "/tmp/emails.csv"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContents` | file | yes | CSV or text file containing email addresses to verify. Example: `/tmp/emails.csv`. |

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

Through the native MillionVerifier API, this operation is `POST https://bulkapi.millionverifier.com/bulkapi/v2/upload` (base URL `https://api.millionverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-verification-file.md) for the provider-specific parameters and requirements.

