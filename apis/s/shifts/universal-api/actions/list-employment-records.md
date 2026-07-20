# 7shifts: List Employment Records

Lists the employment records in 7shifts.

```
GET https://connect.mindcloud.co/v1/universal/shifts/latest/actions/list-employment-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 7shifts `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shifts/latest/actions/list-employment-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shifts/latest/actions/list-employment-records?${params}`, {
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

Through the native 7shifts API, this operation is `GET /v2/company/{company_id}/employment_records` (base URL `https://api.7shifts.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-employment-records.md) for the provider-specific parameters and requirements.

