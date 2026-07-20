# CRM in Cloud: Search appointments

Finds appointments in CRM in Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cRMInCloud/latest/actions/search-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CRM in Cloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRMInCloud/latest/actions/search-appointments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cRMInCloud/latest/actions/search-appointments?${params}`, {
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
      "createdDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | date |  |
| `description` | string |  |
| `endDate` | date |  |
| `id` | number |  |
| `startDate` | date |  |
| `subject` | string |  |

## Native endpoint

Through the native CRM in Cloud API, this operation is `GET /Appointment/Search` (base URL `https://app.crmincloud.it/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-appointments.md) for the provider-specific parameters and requirements.

