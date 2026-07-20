# Lob: Create Check



```
POST https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string",
  "from": "string",
  "bankAccount": "string",
  "amount": 1,
  "message": "string",
  "useType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-check', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string",
    "from": "string",
    "bankAccount": "string",
    "amount": 1,
    "message": "string",
    "useType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional description for the check. |
| `to` | string | yes | Recipient address ID. |
| `from` | string | yes | Sender address ID. |
| `bankAccount` | string | yes | Verified bank account ID. |
| `amount` | number | yes | US dollar amount to send. |
| `message` | string | yes | Text printed at the bottom of the check page. |
| `useType` | string | yes | Declared mail use type. |

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

Through the native Lob API, this operation is `POST /checks` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-check.md) for the provider-specific parameters and requirements.

