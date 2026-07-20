# Snapchat Lead Generation: Create Lead Generation Form

Creates a lead generation form in Snapchat Lead Generation.

```
POST https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-lead-generation-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Lead Generation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-lead-generation-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "adAccountId": "string",
  "leadGenerationForms": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-lead-generation-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "adAccountId": "string",
    "leadGenerationForms": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `adAccountId` | string | yes | The Snapchat Ad Account ID that will own the new lead generation form. |
| `leadGenerationForms` | list<object> | yes | An array of lead generation form objects as documented by Snapchat. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lead_generation_forms": [
        {
          "lead_generation_form": {
            "ad_account_id": "string",
            "created_at": "2026-05-07T12:00:00.000Z",
            "description": "string",
            "end_page_properties": {
              "call_to_action": "string",
              "url": "https://example.com"
            },
            "form_fields": [
              {
                "is_required": true,
                "type": "string"
              }
            ],
            "id": "string",
            "legal_disclosures": {
              "description": "string",
              "title": "string"
            },
            "name": "Ava Chen",
            "privacy_policy_url": "https://example.com",
            "title": "string",
            "updated_at": "2026-05-07T12:00:00.000Z"
          },
          "sub_request_error_reason": "string",
          "sub_request_status": "string"
        }
      ],
      "request_id": "string",
      "request_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lead_generation_forms[].lead_generation_form.ad_account_id` | string |  |
| `lead_generation_forms[].lead_generation_form.created_at` | date |  |
| `lead_generation_forms[].lead_generation_form.description` | string |  |
| `lead_generation_forms[].lead_generation_form.end_page_properties.call_to_action` | string |  |
| `lead_generation_forms[].lead_generation_form.end_page_properties.url` | string |  |
| `lead_generation_forms[].lead_generation_form.form_fields[].is_required` | boolean |  |
| `lead_generation_forms[].lead_generation_form.form_fields[].type` | string |  |
| `lead_generation_forms[].lead_generation_form.id` | string |  |
| `lead_generation_forms[].lead_generation_form.legal_disclosures.description` | string |  |
| `lead_generation_forms[].lead_generation_form.legal_disclosures.title` | string |  |
| `lead_generation_forms[].lead_generation_form.name` | string |  |
| `lead_generation_forms[].lead_generation_form.privacy_policy_url` | string |  |
| `lead_generation_forms[].lead_generation_form.title` | string |  |
| `lead_generation_forms[].lead_generation_form.updated_at` | date |  |
| `lead_generation_forms[].sub_request_error_reason` | string |  |
| `lead_generation_forms[].sub_request_status` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Lead Generation API, this operation is `POST /adaccounts/:adAccountId/lead_generation_forms` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead-generation-form.md) for the provider-specific parameters and requirements.

