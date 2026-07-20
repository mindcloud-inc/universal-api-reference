# ActiveTrail: Update Campaign

Updates an existing campaign in ActiveTrail.

```
PUT https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveTrail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "design": {},
  "details": {},
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "design": {},
    "details": {},
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `a_b_settings` | object | no | A/B settings. |
| `a_b_settings.ab_percent_split_groups` | number | no |  |
| `a_b_settings.google_analytics_name` | string | no |  |
| `a_b_settings.scheduling` | object | no |  |
| `a_b_settings.scheduling.is_sent` | boolean | no |  |
| `a_b_settings.scheduling.scheduled_date_utc` | date | no |  |
| `a_b_settings.subject` | string | no |  |
| `a_b_settings.user_profile_id` | number | no |  |
| `carts` | object | no | E-commerce data list. |
| `carts.ecommerce_data[]` | array<object> | no |  |
| `design` | object | yes | Campaign design. |
| `design.content` | string | no |  |
| `design.header_footer_language_type` | string | no |  |
| `design.is_add_print_email` | boolean | no |  |
| `design.is_auto_css_inliner` | boolean | no |  |
| `design.is_remove_system_links` | boolean | no |  |
| `design.language_type` | string | no |  |
| `details` | object | yes | Campaign details. |
| `details.content_category_id` | number | no |  |
| `details.google_analytics_name` | string | no |  |
| `details.name` | string | no |  |
| `details.predictive_delivery` | boolean | no |  |
| `details.preheader` | string | no |  |
| `details.subject` | string | no |  |
| `details.user_profile_id` | number | no |  |
| `id` | number | yes | Campaign id. |
| `pairs[]` | array<object> | no | Replacement key-value pairs. |
| `pairs[].key` | string | no |  |
| `pairs[].value` | string | no |  |
| `sendTest` | string | no | Email addresses to send a test email to, separated by commas. |
| `template` | object | no | Campaign template. |
| `template.id` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveTrail API returns.

## Native endpoint

Through the native ActiveTrail API, this operation is `PUT /campaigns/:id` (base URL `https://webapi.mymarketing.co.il/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

