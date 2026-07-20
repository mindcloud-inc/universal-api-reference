# TaxBandits: Get W-9

Retrieves a W-9 from TaxBandits.

```
GET https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/get-w9
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/get-w9?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/get-w9?${params}`, {
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
      "FormW9": {},
      "PayeeRef": "string",
      "SubmissionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<object> |  |
| `FormW9` | object |  |
| `PayeeRef` | string |  |
| `SubmissionId` | string |  |

## Native endpoint

Through the native TaxBandits API, this operation is `GET FormW9/Get` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-w9.md) for the provider-specific parameters and requirements.

