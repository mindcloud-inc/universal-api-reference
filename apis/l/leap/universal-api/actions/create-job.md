# Leap: Create Job

Creates a new job in Leap.

```
POST https://connect.mindcloud.co/v1/universal/leap/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leap/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer_id": 1,
  "description": "string",
  "trade_0_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leap/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer_id": 1,
    "description": "string",
    "trade_0_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Street address for the job when not using the customer address. |
| `city` | string | no | City for the job address. |
| `country_id` | number | no | Country ID for the job address. |
| `customer_id` | number | yes | Leap customer ID associated with the job. |
| `description` | string | yes | Description of the job. |
| `name` | string | no | Optional name for the job. |
| `same_as_customer_address` | number | no | Set to 1 to reuse the customer address, or 0 to provide a job-specific address. |
| `state_id` | number | no | State ID for the job address. |
| `trade_0_id` | number | yes | Trade ID to associate with the job. |
| `zip` | number | no | ZIP or postal code for the job address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job` | object | Created job returned by Leap. |
| `message` | string | Provider success message. |
| `status` | number | HTTP-style status code returned by Leap. |

## Native endpoint

Through the native Leap API, this operation is `POST /jobs` (base URL `https://api.jobprogress.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

