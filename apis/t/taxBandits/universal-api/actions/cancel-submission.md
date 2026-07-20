# TaxBandits: Cancel Submission

Cancels an existing submission in TaxBandits.

```
DELETE https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/cancel-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/cancel-submission?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/cancel-submission?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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
      "StatusCode": 1,
      "StatusMessage": "string",
      "StatusName": "Ava Chen",
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
| `StatusCode` | number |  |
| `StatusMessage` | string |  |
| `StatusName` | string |  |
| `SuccessRecords` | array<object> |  |

## Native endpoint

Through the native TaxBandits API, this operation is `POST Utility/CancelSubmission` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-submission.md) for the provider-specific parameters and requirements.

