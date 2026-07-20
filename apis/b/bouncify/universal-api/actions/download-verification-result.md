# Bouncify: Download Verification Result

Downloads a bulk verification result from Bouncify.

```
GET https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/download-verification-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bouncify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/download-verification-result?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/download-verification-result?${params}`, {
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
| `jobId` | string | yes | Bulk verification job id to download. |
| `filterResult` | string | no | Optional result categories to include in the download. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Downloaded bulk-results CSV content returned by Bouncify. |

## Native endpoint

Through the native Bouncify API, this operation is `POST /download` (base URL `https://api.bouncify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-verification-result.md) for the provider-specific parameters and requirements.

