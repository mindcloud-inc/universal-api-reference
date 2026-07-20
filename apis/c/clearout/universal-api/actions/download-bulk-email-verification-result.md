# Clearout: Download Bulk Email Verification Result

Retrieves a bulk email verification result download from Clearout.

```
GET https://connect.mindcloud.co/v1/universal/clearout/latest/actions/download-bulk-email-verification-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clearout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/download-bulk-email-verification-result?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearout/latest/actions/download-bulk-email-verification-result?${params}`, {
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
| `listId` | string | yes | Pass the value of bulk list_id property from response object |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native Clearout API, this operation is `POST /download/result` (base URL `https://api.clearout.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-bulk-email-verification-result.md) for the provider-specific parameters and requirements.

