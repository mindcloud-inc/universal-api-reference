# MillionVerifier: Delete Verification File

Deletes a verification file from MillionVerifier.

```
DELETE https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/delete-verification-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MillionVerifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/delete-verification-file?connectionId=$CONNECTION_ID&fileId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/delete-verification-file?${params}`, {
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
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native MillionVerifier API, this operation is `GET https://bulkapi.millionverifier.com/bulkapi/v2/delete` (base URL `https://api.millionverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-verification-file.md) for the provider-specific parameters and requirements.

