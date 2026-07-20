# Rubitime: Get Record

Retrieves a record from Rubitime.

```
GET https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/get-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rubitime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/get-record?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/get-record?${params}`, {
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
| `id` | number | yes | Rubitime record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "duration": 1,
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "phone": "string",
      "price": 1,
      "record": "string",
      "status": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string | Customer comment. |
| `duration` | number | Service duration in minutes. |
| `email` | string | Customer email. |
| `id` | number | Record ID. |
| `name` | string | Customer name. |
| `phone` | string | Customer phone. |
| `price` | number | Service price. |
| `record` | string | Scheduled record date and time. |
| `status` | number | Record status. |
| `url` | string | Record URL. |

## Native endpoint

Through the native Rubitime API, this operation is `POST /get-record` (base URL `https://rubitime.ru/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record.md) for the provider-specific parameters and requirements.

