# Lob: Create Postcard



```
POST https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-postcard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-postcard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string",
  "from": "string",
  "front": "string",
  "back": "string",
  "useType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-postcard', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string",
    "from": "string",
    "front": "string",
    "back": "string",
    "useType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional description for the postcard job. |
| `to` | string | yes | Recipient address ID. |
| `from` | string | yes | Sender address ID or inline US address. |
| `front` | string | yes | Front artwork for the postcard. |
| `back` | string | yes | Back artwork for the postcard. |
| `useType` | string | yes | Declared mail use type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "back_template_id": "string",
      "back_template_version_id": "string",
      "campaign_id": "string",
      "carrier": "string",
      "completed_at": "string",
      "date_created": "string",
      "date_modified": "string",
      "description": "string",
      "expected_delivery_date": "string",
      "failure_reason": "string",
      "from": {},
      "front_template_id": "string",
      "front_template_version_id": "string",
      "fsc": true,
      "id": "string",
      "is_creative_proof": true,
      "is_dashboard": true,
      "lob_credits_funding_status": "string",
      "mail_type": "string",
      "merge_variables": {},
      "metadata": {},
      "object": "string",
      "print_speed": "string",
      "qr_code": "string",
      "raw_url": "https://example.com",
      "send_date": "string",
      "size": "string",
      "status": "string",
      "thumbnails": [
        {}
      ],
      "to": {},
      "to_be_expunged_date": "string",
      "tracking_events": [
        {}
      ],
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
| `back_template_id` | string |  |
| `back_template_version_id` | string |  |
| `campaign_id` | string |  |
| `carrier` | string |  |
| `completed_at` | string |  |
| `date_created` | string |  |
| `date_modified` | string |  |
| `description` | string |  |
| `expected_delivery_date` | string |  |
| `failure_reason` | string |  |
| `from` | object |  |
| `front_template_id` | string |  |
| `front_template_version_id` | string |  |
| `fsc` | boolean |  |
| `id` | string |  |
| `is_creative_proof` | boolean |  |
| `is_dashboard` | boolean |  |
| `lob_credits_funding_status` | string |  |
| `mail_type` | string |  |
| `merge_variables` | object |  |
| `metadata` | object |  |
| `object` | string |  |
| `print_speed` | string |  |
| `qr_code` | string |  |
| `raw_url` | string |  |
| `send_date` | string |  |
| `size` | string |  |
| `status` | string |  |
| `thumbnails` | array<object> |  |
| `to` | object |  |
| `to_be_expunged_date` | string |  |
| `tracking_events` | array<object> |  |
| `url` | string |  |
| `use_type` | string |  |
| `usps_campaign_id` | string |  |

## Native endpoint

Through the native Lob API, this operation is `POST /postcards` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-postcard.md) for the provider-specific parameters and requirements.

