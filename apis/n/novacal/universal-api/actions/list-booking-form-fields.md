# Novacal: List Booking Form Fields

Retrieves booking form fields from Novacal.

```
GET https://connect.mindcloud.co/v1/universal/novacal/latest/actions/list-booking-form-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novacal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/list-booking-form-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novacal/latest/actions/list-booking-form-fields?${params}`, {
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
      "id": 1,
      "identifier": "string",
      "is_active": true,
      "is_required": true,
      "label": "string",
      "options": [
        "string"
      ],
      "placeholder": "string",
      "position": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Booking form field ID. |
| `identifier` | string | Field identifier. |
| `is_active` | boolean | Whether the field is active. |
| `is_required` | boolean | Whether the field is required. |
| `label` | string | Field label. |
| `options` | array<string> | Choice options. |
| `placeholder` | string | Placeholder text. |
| `position` | number | Field display position. |
| `type` | string | Field type. |

## Native endpoint

Through the native Novacal API, this operation is `GET /v1/event-types/:eventType/booking-forms` (base URL `https://api.novacal.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-booking-form-fields.md) for the provider-specific parameters and requirements.

