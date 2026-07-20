# Scanova: Get QR Code List



```
GET https://connect.mindcloud.co/v1/universal/scanova/latest/actions/get-qr-code-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/get-qr-code-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scanova/latest/actions/get-qr-code-list?${params}`, {
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
| `createdFrom` | date | no | Filter QR codes created from this date (YYYY-MM-DD) |
| `createdTill` | date | no | Filter QR codes created till this date (YYYY-MM-DD) |
| `search` | string | no | Search value |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `qrid` | string | no | Filter by specific QR code ID(s). Must be a comma-separated list of QR IDs. Example: Q349...,Qf94... Accepts multiple values in one string, delimited by `,`. |
| `tags` | string | no | Filter by tags (comma-separated, URL encoded) Accepts multiple values in one string, delimited by `,`. |
| `category` | string | no | Filter by category slugs (comma-separated, URL encoded) Accepts multiple values in one string, delimited by `,`. |
| `type` | string | no | Filter by QR code type |
| `status` | string | no | Filter by QR code status |
| `users` | string | no | Filter by user IDs (comma-separated, URL encoded) Accepts multiple values in one string, delimited by `,`. |
| `scanType` | string | no | Filter by scan count comparison type |
| `scanCount1` | number | no | Primary scan count value (required with scan_type) |
| `scanCount2` | number | no | Secondary scan count value (required for 'between' scan_type) |
| `searchFields` | string | no | Fields to search in (comma-separated) Accepts multiple values in one string, delimited by `,`. |

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

Through the native Scanova API, this operation is `GET /qr/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-qr-code-list.md) for the provider-specific parameters and requirements.

