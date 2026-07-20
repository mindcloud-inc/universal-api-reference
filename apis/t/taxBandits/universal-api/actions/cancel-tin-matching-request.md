# TaxBandits: Cancel TIN Matching Request

Cancels a TIN matching request in TaxBandits.

```
PUT https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/cancel-tin-matching-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/cancel-tin-matching-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/cancel-tin-matching-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "ErrorRecords": [
        {}
      ],
      "Errors": [
        {}
      ],
      "SubmissionId": "string",
      "SuccessRecords": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ErrorRecords` | array<object> |  |
| `Errors` | array<object> |  |
| `SubmissionId` | string |  |
| `SuccessRecords` | array<object> |  |

## Native endpoint

Through the native TaxBandits API, this operation is `PUT TINMatchingRecipients/CancelRequest` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-tin-matching-request.md) for the provider-specific parameters and requirements.

