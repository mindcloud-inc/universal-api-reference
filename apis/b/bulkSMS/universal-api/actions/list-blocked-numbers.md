# BulkSMS: List Blocked Numbers

Retrieves blocked phone numbers from BulkSMS.

```
GET https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/list-blocked-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/list-blocked-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/list-blocked-numbers?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `minId` | number | no | Return blocked-number records with an ID greater than or equal to this value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "phoneNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `description` | string |  |
| `id` | number |  |
| `phoneNumber` | string |  |

## Native endpoint

Through the native BulkSMS API, this operation is `GET /blocked-numbers` (base URL `https://api.bulksms.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-blocked-numbers.md) for the provider-specific parameters and requirements.

