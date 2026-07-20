# Google Ads: Add Offline User Data Job Operations

Adds operations to an offline user data job in Google Ads.

```
PUT https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/add-offline-user-data-job-operations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/add-offline-user-data-job-operations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "1234567890",
  "offlineUserDataJobId": "1111111111",
  "operations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/add-offline-user-data-job-operations', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "1234567890",
    "offlineUserDataJobId": "1111111111",
    "operations[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | list | yes | Customer ID that owns the Google Ads resources (without dashes). Example: `1234567890`. |
| `offlineUserDataJobId` | string | yes | Offline user data job ID to append operations to. Example: `1111111111`. |
| `operations[]` | array<object> | yes | Offline user data job operations to add. |

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
      "warning": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `partialFailureError` | object | Partial failure status returned when individual offline user data job operations fail. |
| `warning` | object | Non-blocking warning details returned when warnings mode is enabled. |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/offlineUserDataJobs/:offlineUserDataJobId:addOperations` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-offline-user-data-job-operations.md) for the provider-specific parameters and requirements.

