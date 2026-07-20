# Google Ads: Upload Conversion Adjustments

Uploads conversion adjustments to Google Ads.

```
PUT https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/upload-conversion-adjustments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/upload-conversion-adjustments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversionAdjustments[]": [
    "string"
  ],
  "customerId": "1234567890",
  "partialFailure": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/upload-conversion-adjustments', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversionAdjustments[]": ["string"],
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
| `conversionAdjustments[]` | array | yes | Conversion adjustment rows to upload. |
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
      "jobId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId:uploadConversionAdjustments` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-conversion-adjustments.md) for the provider-specific parameters and requirements.

