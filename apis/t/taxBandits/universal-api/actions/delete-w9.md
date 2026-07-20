# TaxBandits: Delete W-9

Deletes a W-9 from TaxBandits.

```
DELETE https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/delete-w9
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/delete-w9?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/delete-w9?${params}`, {
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
| `email` | string | no | Payee email. |
| `payeeRef` | string | no | Payee reference. |
| `submissionId` | string | no | Submission identifier. |

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
| `PayeeRef` | string |  |
| `SubmissionId` | string |  |

## Native endpoint

Through the native TaxBandits API, this operation is `DELETE FormW9/Delete` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-w9.md) for the provider-specific parameters and requirements.

