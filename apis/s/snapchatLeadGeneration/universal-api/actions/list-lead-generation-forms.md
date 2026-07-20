# Snapchat Lead Generation: List Lead Generation Forms

Retrieves lead generation forms from Snapchat Lead Generation.

```
GET https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/list-lead-generation-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Lead Generation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/list-lead-generation-forms?connectionId=$CONNECTION_ID&adAccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adAccountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/list-lead-generation-forms?${params}`, {
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
| `adAccountId` | string | yes | The Snapchat Ad Account ID that owns the lead generation forms. |

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
            "banner_media_id": "string",
            "created_at": "2026-05-07T12:00:00.000Z",
            "description": "string",
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
            "strategy_type": "string",
            "title": "string",
            "updated_at": "2026-05-07T12:00:00.000Z"
          },
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
| `lead_generation_forms[].lead_generation_form.banner_media_id` | string |  |
| `lead_generation_forms[].lead_generation_form.created_at` | date |  |
| `lead_generation_forms[].lead_generation_form.description` | string |  |
| `lead_generation_forms[].lead_generation_form.form_fields[].is_required` | boolean |  |
| `lead_generation_forms[].lead_generation_form.form_fields[].type` | string |  |
| `lead_generation_forms[].lead_generation_form.id` | string |  |
| `lead_generation_forms[].lead_generation_form.legal_disclosures.description` | string |  |
| `lead_generation_forms[].lead_generation_form.legal_disclosures.title` | string |  |
| `lead_generation_forms[].lead_generation_form.name` | string |  |
| `lead_generation_forms[].lead_generation_form.privacy_policy_url` | string |  |
| `lead_generation_forms[].lead_generation_form.strategy_type` | string |  |
| `lead_generation_forms[].lead_generation_form.title` | string |  |
| `lead_generation_forms[].lead_generation_form.updated_at` | date |  |
| `lead_generation_forms[].sub_request_status` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Lead Generation API, this operation is `GET /adaccounts/:adAccountId/lead_generation_forms` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lead-generation-forms.md) for the provider-specific parameters and requirements.

