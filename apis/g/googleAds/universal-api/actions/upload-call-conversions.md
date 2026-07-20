# Google Ads: Upload Call Conversions

Uploads call conversions to Google Ads.

```
POST https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/upload-call-conversions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/upload-call-conversions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversions[]": [
    "string"
  ],
  "customerId": "1234567890",
  "partialFailure": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/upload-call-conversions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversions[]": ["string"],
    "customerId": "1234567890",
    "partialFailure": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversions[]` | array | yes | Call conversion rows to upload. |
| `customerId` | list | yes | Customer ID that owns the Google Ads resources (without dashes). Example: `1234567890`. |
| `partialFailure` | boolean | yes | Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `validateOnly` | boolean | no | When true, validates the request without executing mutations. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "partialFailureError": {},
      "results": [
        {
          "callerId": "string",
          "callStartDateTime": "string",
          "conversionAction": "string",
          "conversionDateTime": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `partialFailureError` | object | Partial failure status returned when individual call conversion rows fail. |
| `results[].callerId` | string | Caller phone number for a successfully processed call conversion. |
| `results[].callStartDateTime` | string | Call start date-time for a successfully processed call conversion. |
| `results[].conversionAction` | string | Conversion action resource name for the uploaded call conversion. |
| `results[].conversionDateTime` | string | Conversion date-time for the uploaded call conversion. |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId:uploadCallConversions` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-call-conversions.md) for the provider-specific parameters and requirements.

