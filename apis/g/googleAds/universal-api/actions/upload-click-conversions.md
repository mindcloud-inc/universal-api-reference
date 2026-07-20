# Google Ads: Upload Click Conversions

Uploads click conversions to Google Ads.

```
POST https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/upload-click-conversions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/upload-click-conversions" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/upload-click-conversions', {
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
| `conversions[]` | array | yes | Click conversion rows to upload. |
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

Through the native Google Ads API, this operation is `POST v22/customers/:customerId:uploadClickConversions` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-click-conversions.md) for the provider-specific parameters and requirements.

