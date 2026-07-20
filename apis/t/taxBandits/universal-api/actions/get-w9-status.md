# TaxBandits: Get W-9 Status

Retrieves W-9 status from TaxBandits.

```
GET https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/get-w9-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/get-w9-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/get-w9-status?${params}`, {
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
| `businessId` | string | no | Business identifier. |
| `email` | string | no | Payee email. |
| `payeeRef` | string | no | Payee reference. |
| `tin` | string | no | Business EIN or SSN. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        {}
      ],
      "PayeeRef": "string",
      "StatusTs": "string",
      "SubmissionId": "string",
      "W9Status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<object> |  |
| `PayeeRef` | string |  |
| `StatusTs` | string |  |
| `SubmissionId` | string |  |
| `W9Status` | string |  |

## Native endpoint

Through the native TaxBandits API, this operation is `GET FormW9/Status` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-w9-status.md) for the provider-specific parameters and requirements.

