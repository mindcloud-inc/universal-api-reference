# ServiceM8: Create Job Allocation



```
POST https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-job-allocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-job-allocation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "allocationWindowUuid": "123e4567-e89b-12d3-a456-426614174000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-job-allocation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "allocationWindowUuid": "123e4567-e89b-12d3-a456-426614174000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobUuid` | string | no | Example: `123e4567-e89b-12d3-a456-426614174000`. |
| `staffUuid` | string | no | Example: `123e4567-e89b-12d3-a456-426614174000`. |
| `allocationDate` | date | no | Example: `2026-03-01 12:00:00`. |
| `allocationWindowUuid` | string | yes | Required ServiceM8 allocation window UUID. Retrieve this from the Allocation Windows resource configured in the connected ServiceM8 tenant. Example: `123e4567-e89b-12d3-a456-426614174000`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortPriority` | string | no | Example: `10`. |
| `allocatedByStaffUuid` | string | no | Example: `123e4567-e89b-12d3-a456-426614174000`. |
| `allocatedTimestamp` | date | no | Example: `2026-03-01 11:55:00`. |
| `expiryTimestamp` | date | no | Example: `2026-03-01 18:00:00`. |
| `readTimestamp` | date | no | Example: `2026-03-01 12:05:00`. |
| `completionTimestamp` | date | no | Example: `2026-03-01 15:00:00`. |
| `uuid` | string | no | Example: `123e4567-e89b-12d3-a456-426614174000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recordUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recordUuid` | string | UUID of the created job allocation. |

## Native endpoint

Through the native ServiceM8 API, this operation is `POST /api_1.0/joballocation.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job-allocation.md) for the provider-specific parameters and requirements.

