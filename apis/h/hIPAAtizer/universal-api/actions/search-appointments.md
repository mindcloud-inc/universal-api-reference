# HIPAAtizer: Search Appointments

Finds appointments in HIPAAtizer by location, service, or date.

```
GET https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/search-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HIPAAtizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/search-appointments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/search-appointments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request.search` | string | no | Search term. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request` | object | no | Optional raw request wrapper. Use `{}` when running without filters. |
| `request.dateRange.from` | string | no | Start date filter. |
| `request.dateRange.to` | string | no | End date filter. |
| `request.locationIds` | list<string> | no | Optional location UUID filters. |
| `request.pagination.limit` | number | no | Pagination page size. |
| `request.pagination.page` | number | no | Pagination page number. |
| `request.serviceIds` | list<string> | no | Optional service UUID filters. |
| `request.workerIds` | list<string> | no | Optional worker UUID filters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": "string",
        "date": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "haveRelatedSubmission": true,
        "id": "string",
        "lastName": "Chen",
        "location": {
          "id": "string",
          "name": "Ava Chen"
        },
        "phone": "string",
        "service": {
          "id": "string",
          "title": "string"
        },
        "worker": {
          "id": "string",
          "name": "Ava Chen"
        }
      },
      "pagination": {
        "limit": 1,
        "page": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createdAt` | string |  |
| `data.date` | string |  |
| `data.email` | string |  |
| `data.firstName` | string |  |
| `data.haveRelatedSubmission` | boolean |  |
| `data.id` | string |  |
| `data.lastName` | string |  |
| `data.location.id` | string |  |
| `data.location.name` | string |  |
| `data.phone` | string |  |
| `data.service.id` | string |  |
| `data.service.title` | string |  |
| `data.worker.id` | string |  |
| `data.worker.name` | string |  |
| `pagination.limit` | number |  |
| `pagination.page` | number |  |
| `pagination.total` | number |  |

## Native endpoint

Through the native HIPAAtizer API, this operation is `POST /api/v1/api_key/appointments/search` (base URL `https://app.hipaatizer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-appointments.md) for the provider-specific parameters and requirements.

