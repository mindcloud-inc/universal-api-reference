# Scanova: Attach Or Detach Lead List



```
PUT https://connect.mindcloud.co/v1/universal/scanova/latest/actions/attach-or-detach-lead-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/attach-or-detach-lead-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "qrid": "string",
  "leadList": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scanova/latest/actions/attach-or-detach-lead-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "qrid": "string",
    "leadList": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `qrid` | string | yes | QR code ID |
| `leadList` | string | yes | Set to null to detach lead list from QR code |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ai_qr_code": "string",
      "category": {},
      "created": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "custom_form_response_count": 1,
      "dynamic_url_object": {},
      "id": 1,
      "info": "string",
      "is_active": true,
      "is_age_restricted": true,
      "is_designer": true,
      "is_password_protected": true,
      "is_qr_scannable": true,
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "password": "string",
      "pattern_info": "string",
      "pattern_type": "string",
      "qr_type": "string",
      "qr_type_display": "string",
      "qrid": "string",
      "restaurant_feedback_response_count": 1,
      "rsvp_form_response_count": 1,
      "svg_code": "string",
      "tags_list": [
        "string"
      ],
      "thumbnail": "string",
      "version": 1,
      "wallet_pass_info": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_qr_code` | string |  |
| `category` | object |  |
| `created` | date |  |
| `created_by` | string |  |
| `custom_form_response_count` | number |  |
| `dynamic_url_object` | object |  |
| `id` | number |  |
| `info` | string |  |
| `is_active` | boolean |  |
| `is_age_restricted` | boolean |  |
| `is_designer` | boolean |  |
| `is_password_protected` | boolean |  |
| `is_qr_scannable` | boolean |  |
| `modified` | date |  |
| `name` | string |  |
| `password` | string |  |
| `pattern_info` | string |  |
| `pattern_type` | string |  |
| `qr_type` | string |  |
| `qr_type_display` | string |  |
| `qrid` | string |  |
| `restaurant_feedback_response_count` | number |  |
| `rsvp_form_response_count` | number |  |
| `svg_code` | string |  |
| `tags_list` | array<string> |  |
| `thumbnail` | string |  |
| `version` | number |  |
| `wallet_pass_info` | string |  |

## Native endpoint

Through the native Scanova API, this operation is `PATCH /qr/{qrid}/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attach-or-detach-lead-list.md) for the provider-specific parameters and requirements.

