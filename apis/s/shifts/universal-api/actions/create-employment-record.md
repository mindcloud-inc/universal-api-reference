# 7shifts: Create Employment Record

Creates a new employment record in 7shifts.

```
POST https://connect.mindcloud.co/v1/universal/shifts/latest/actions/create-employment-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 7shifts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shifts/latest/actions/create-employment-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shifts/latest/actions/create-employment-record', {
  method: 'POST',
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
      "employment_type": "string",
      "hire_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "status": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `employment_type` | string |  |
| `hire_date` | date |  |
| `id` | number |  |
| `status` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native 7shifts API, this operation is `POST /v2/company/{company_id}/employment_records` (base URL `https://api.7shifts.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-employment-record.md) for the provider-specific parameters and requirements.

