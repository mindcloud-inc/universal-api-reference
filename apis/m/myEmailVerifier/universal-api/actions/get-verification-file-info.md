# MyEmailVerifier: Get Verification File Info

Retrieves bulk verification job details from MyEmailVerifier.

```
GET https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/get-verification-file-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyEmailVerifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/get-verification-file-info?connectionId=$CONNECTION_ID&fileId=257866" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "257866"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/get-verification-file-info?${params}`, {
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
| `fileId` | number | yes | Bulk verification file ID returned by Upload Verification File. Example: `257866`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": {},
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | object | Bulk verification job details, counts, and report URLs. |
| `status` | boolean | Whether the file info request succeeded. |

## Native endpoint

Through the native MyEmailVerifier API, this operation is `GET /verifier/file_info/{{credentials.apiKey}}/:fileId` (base URL `https://client.myemailverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-verification-file-info.md) for the provider-specific parameters and requirements.

