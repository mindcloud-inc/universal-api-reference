# Lob: Create Letter



```
POST https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-letter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-letter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string",
  "from": "string",
  "file": "string",
  "color": true,
  "useType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-letter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string",
    "from": "string",
    "file": "string",
    "color": true,
    "useType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional description for the letter job. |
| `to` | string | yes | Recipient address ID. |
| `from` | string | yes | Sender address ID. |
| `file` | string | yes | Letter artwork file, template ID, HTML, or remote file URL. |
| `color` | boolean | yes | Whether to print the letter in color. |
| `useType` | string | yes | Declared mail use type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address_placement": "string",
      "campaign_id": "string",
      "carrier": "string",
      "color": true,
      "completed_at": "string",
      "custom_envelope": "string",
      "date_created": "string",
      "date_modified": "string",
      "description": "string",
      "double_sided": true,
      "expected_delivery_date": "string",
      "extra_service": "string",
      "failure_reason": "string",
      "from": {},
      "fsc": true,
      "id": "string",
      "is_creative_proof": true,
      "is_dashboard": true,
      "lob_credits_funding_status": "string",
      "mail_type": "string",
      "merge_variables": {},
      "metadata": {},
      "object": "string",
      "perforated_page": "string",
      "print_speed": "string",
      "qr_code": "string",
      "raw_url": "https://example.com",
      "return_envelope": true,
      "send_date": "string",
      "status": "string",
      "template_id": "string",
      "template_version_id": "string",
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
| `address_placement` | string |  |
| `campaign_id` | string |  |
| `carrier` | string |  |
| `color` | boolean |  |
| `completed_at` | string |  |
| `custom_envelope` | string |  |
| `date_created` | string |  |
| `date_modified` | string |  |
| `description` | string |  |
| `double_sided` | boolean |  |
| `expected_delivery_date` | string |  |
| `extra_service` | string |  |
| `failure_reason` | string |  |
| `from` | object |  |
| `fsc` | boolean |  |
| `id` | string |  |
| `is_creative_proof` | boolean |  |
| `is_dashboard` | boolean |  |
| `lob_credits_funding_status` | string |  |
| `mail_type` | string |  |
| `merge_variables` | object |  |
| `metadata` | object |  |
| `object` | string |  |
| `perforated_page` | string |  |
| `print_speed` | string |  |
| `qr_code` | string |  |
| `raw_url` | string |  |
| `return_envelope` | boolean |  |
| `send_date` | string |  |
| `status` | string |  |
| `template_id` | string |  |
| `template_version_id` | string |  |
| `thumbnails` | array<object> |  |
| `to` | object |  |
| `to_be_expunged_date` | string |  |
| `tracking_events` | array<object> |  |
| `tracking_number` | string |  |
| `url` | string |  |
| `use_type` | string |  |
| `usps_campaign_id` | string |  |

## Native endpoint

Through the native Lob API, this operation is `POST /letters` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-letter.md) for the provider-specific parameters and requirements.

