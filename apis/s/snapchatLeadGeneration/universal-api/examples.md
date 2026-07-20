# Snapchat Lead Generation Universal API Examples

These examples use the MindCloud API key and Snapchat Lead Generation connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lead Generation Forms

Retrieves lead generation forms from Snapchat Lead Generation.

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

Example response:

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

See the full [List Lead Generation Forms action reference](actions/list-lead-generation-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/snapchatLeadGeneration/latest/actions/list-lead-generation-forms).

## Create Lead Generation Ad

Creates a lead generation ad in Snapchat Lead Generation.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-lead-generation-ad" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "adSquadId": "string",
  "ads": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-lead-generation-ad', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "adSquadId": "string",
    "ads": {}
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "ads": [
        {
          "ad": {
            "ad_squad_id": "string",
            "approval_type": "string",
            "creative_id": "string",
            "delivery_status": [
              "string"
            ],
            "effective_status": "string",
            "id": "string",
            "name": "Ava Chen",
            "render_type": "string",
            "review_status": "string",
            "status": "string",
            "type": "string"
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

See the full [Create Lead Generation Ad action reference](actions/create-lead-generation-ad.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/snapchatLeadGeneration/latest/actions/create-lead-generation-ad).
