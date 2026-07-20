# OpenRegister: Get Realtime Document

Retrieves a realtime company document from OpenRegister.

```
GET https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-realtime-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRegister `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-realtime-document?connectionId=$CONNECTION_ID&companyId=DE-HRB-D2601-145602&documentCategory=current_printout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "DE-HRB-D2601-145602",
  "documentCategory": "current_printout"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-realtime-document?${params}`, {
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
| `companyId` | string | yes | Company ID to retrieve a realtime document for. Example: `DE-HRB-D2601-145602`. |
| `documentCategory` | string | yes | Document category to retrieve. Default: `current_printout`. Example: `current_printout`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "file_date": "2026-05-07T12:00:00.000Z",
      "file_name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Document category. |
| `file_date` | date | Document file date. |
| `file_name` | string | Document file name. |
| `url` | string | Download URL for the realtime document. |

## Native endpoint

Through the native OpenRegister API, this operation is `GET /v1/document` (base URL `https://api.openregister.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-realtime-document.md) for the provider-specific parameters and requirements.

