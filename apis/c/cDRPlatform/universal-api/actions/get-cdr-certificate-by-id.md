# CDR Platform: Get CDR Certificate By ID

Retrieves a CDR certificate by ID from CDR Platform.

```
GET https://connect.mindcloud.co/v1/universal/cDRPlatform/latest/actions/get-cdr-certificate-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CDR Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cDRPlatform/latest/actions/get-cdr-certificate-by-id?connectionId=$CONNECTION_ID&id=ABC-DEF-GHI" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "ABC-DEF-GHI"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cDRPlatform/latest/actions/get-cdr-certificate-by-id?${params}`, {
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
| `id` | string | yes | Certificate ID using the documented three-part code format, for example ABC-DEF-GHI. Example: `ABC-DEF-GHI`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "certificate_id": "string",
      "display_name": "Ava Chen",
      "issued_date": "2026-05-07T12:00:00.000Z",
      "removal_amount_kg": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certificate_id` | string | Certificate identifier. |
| `display_name` | string | Certificate display name. |
| `issued_date` | date | Date the certificate was issued. |
| `removal_amount_kg` | number | Removal amount in kilograms. |

## Native endpoint

Through the native CDR Platform API, this operation is `GET /v1/certificate/:id/` (base URL `https://api.cdrplatform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cdr-certificate-by-id.md) for the provider-specific parameters and requirements.

