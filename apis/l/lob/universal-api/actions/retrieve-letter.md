# Lob: Retrieve Letter



```
GET https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-letter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-letter?connectionId=$CONNECTION_ID&ltr_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ltr_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-letter?${params}`, {
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
| `ltr_id` | string | yes | The Lob letter ID to retrieve. |

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

Through the native Lob API, this operation is `GET /letters/:ltr_id` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-letter.md) for the provider-specific parameters and requirements.

