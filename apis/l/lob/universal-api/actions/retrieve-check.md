# Lob: Retrieve Check



```
GET https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-check?connectionId=$CONNECTION_ID&chk_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chk_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-check?${params}`, {
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
| `chk_id` | string | yes | The Lob check ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "attachment_template_id": "string",
      "attachment_template_version_id": "string",
      "bank_account": {},
      "carrier": "string",
      "check_bottom_template_id": "string",
      "check_bottom_template_version_id": "string",
      "check_number": 1,
      "color": true,
      "completed_at": "string",
      "date_created": "string",
      "date_modified": "string",
      "description": "string",
      "expected_delivery_date": "string",
      "failure_reason": "string",
      "from": {},
      "id": "string",
      "is_dashboard": true,
      "lob_credits_funding_status": "string",
      "mail_type": "string",
      "memo": "string",
      "merge_variables": {},
      "message": "string",
      "metadata": {},
      "object": "string",
      "print_speed": "string",
      "raw_url": "https://example.com",
      "send_date": "string",
      "status": "string",
      "thumbnails": [
        {}
      ],
      "to": {},
      "to_be_expunged_date": "string",
      "tracking_events": [
        {}
      ],
      "tracking_number": "string",
      "url": "https://example.com",
      "use_type": "string",
      "usps_campaign_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `attachment_template_id` | string |  |
| `attachment_template_version_id` | string |  |
| `bank_account` | object |  |
| `carrier` | string |  |
| `check_bottom_template_id` | string |  |
| `check_bottom_template_version_id` | string |  |
| `check_number` | number |  |
| `color` | boolean |  |
| `completed_at` | string |  |
| `date_created` | string |  |
| `date_modified` | string |  |
| `description` | string |  |
| `expected_delivery_date` | string |  |
| `failure_reason` | string |  |
| `from` | object |  |
| `id` | string |  |
| `is_dashboard` | boolean |  |
| `lob_credits_funding_status` | string |  |
| `mail_type` | string |  |
| `memo` | string |  |
| `merge_variables` | object |  |
| `message` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `print_speed` | string |  |
| `raw_url` | string |  |
| `send_date` | string |  |
| `status` | string |  |
| `thumbnails` | array<object> |  |
| `to` | object |  |
| `to_be_expunged_date` | string |  |
| `tracking_events` | array<object> |  |
| `tracking_number` | string |  |
| `url` | string |  |
| `use_type` | string |  |
| `usps_campaign_id` | string |  |

## Native endpoint

Through the native Lob API, this operation is `GET /checks/:chk_id` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-check.md) for the provider-specific parameters and requirements.

