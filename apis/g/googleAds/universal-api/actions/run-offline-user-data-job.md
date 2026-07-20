# Google Ads: Run Offline User Data Job

Runs an offline user data job in Google Ads.

```
PUT https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/run-offline-user-data-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/run-offline-user-data-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "1234567890",
  "offlineUserDataJobId": "1111111111"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/run-offline-user-data-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "1234567890",
    "offlineUserDataJobId": "1111111111"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | list | yes | Customer ID that owns the Google Ads resources (without dashes). Example: `1234567890`. |
| `offlineUserDataJobId` | string | yes | Offline user data job ID to run. Example: `1111111111`. |

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
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/offlineUserDataJobs/:offlineUserDataJobId:run` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-offline-user-data-job.md) for the provider-specific parameters and requirements.

