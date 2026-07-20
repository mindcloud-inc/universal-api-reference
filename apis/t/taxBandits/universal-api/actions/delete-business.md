# TaxBandits: Delete Business

Deletes an existing business from TaxBandits.

```
DELETE https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/delete-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/delete-business?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/delete-business?${params}`, {
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
| `businessId` | string | no | TaxBandits business identifier. |
| `einOrSsn` | string | no | Business EIN or SSN. |
| `isForceDelete` | string | no | Set true to force deletion where supported. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BusinessId": "string",
      "Errors": [
        {}
      ],
      "StatusCode": 1,
      "StatusMessage": "string",
      "StatusName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BusinessId` | string |  |
| `Errors` | array<object> |  |
| `StatusCode` | number |  |
| `StatusMessage` | string |  |
| `StatusName` | string |  |

## Native endpoint

Through the native TaxBandits API, this operation is `DELETE Business/Delete` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-business.md) for the provider-specific parameters and requirements.

