# Veryfi: Delete a Tls Certificate

Deletes a TLS certificate from Veryfi.

```
DELETE https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/delete-api-v8-partner-settings-tls-certificate-certificate-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/delete-api-v8-partner-settings-tls-certificate-certificate-id?connectionId=$CONNECTION_ID&certificateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "certificateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/delete-api-v8-partner-settings-tls-certificate-certificate-id?${params}`, {
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
| `certificateId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": [
        {}
      ],
      "error": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | array<object> |  |
| `error` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `DELETE /api/v8/partner/settings/tls-certificate/:certificate_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-api-v8-partner-settings-tls-certificate-certificate-id.md) for the provider-specific parameters and requirements.

