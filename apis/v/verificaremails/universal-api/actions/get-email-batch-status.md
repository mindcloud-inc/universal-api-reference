# Verificaremails: Get Email Batch Status

Retrieves an email batch validation status from Verificaremails.

```
GET https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/get-email-batch-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verificaremails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/get-email-batch-status?connectionId=$CONNECTION_ID&requestId=6453963" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "6453963"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/get-email-batch-status?${params}`, {
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
| `requestId` | string | yes | Batch request ID returned when the email batch validation was created. Example: `6453963`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": {},
      "dateCreated": "string",
      "dateUpdated": "string",
      "download": "https://example.com",
      "items": {},
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | object | Billed and unbilled credits for the processed email batch. |
| `dateCreated` | string | Provider-reported batch creation timestamp. |
| `dateUpdated` | string | Provider-reported batch update timestamp. |
| `download` | string | Download URL for the completed batch results when available. |
| `items` | object | Batch item counts grouped by total, processed, and pending items. |
| `name` | string | Uploaded file name associated with the batch request. |
| `status` | string | Current provider processing status for the email batch request. |

## Native endpoint

Through the native Verificaremails API, this operation is `GET /email/status/{{requestId}}` (base URL `https://dashboard.verificaremails.com/myapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-batch-status.md) for the provider-specific parameters and requirements.

