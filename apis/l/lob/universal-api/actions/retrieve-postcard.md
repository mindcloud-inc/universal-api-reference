# Lob: Retrieve Postcard



```
GET https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-postcard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-postcard?connectionId=$CONNECTION_ID&psc_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "psc_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-postcard?${params}`, {
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
| `psc_id` | string | yes | The Lob postcard ID to retrieve. |

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

Through the native Lob API, this operation is `GET /postcards/:psc_id` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-postcard.md) for the provider-specific parameters and requirements.

