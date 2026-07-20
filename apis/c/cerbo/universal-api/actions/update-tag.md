# Cerbo: Update Tag

Updates an existing tag in Cerbo.

```
PUT https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tag_id": 1,
  "name": "Ava Chen",
  "category": "string",
  "description": "string",
  "displays_on_dash": true,
  "note_displays_on_dashboard": true,
  "displays_on_calendar": true,
  "color": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tag_id": 1,
    "name": "Ava Chen",
    "category": "string",
    "description": "string",
    "displays_on_dash": true,
    "note_displays_on_dashboard": true,
    "displays_on_calendar": true,
    "color": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tag_id` | number | yes | ID of tag to update |
| `name` | string | yes | Name of the tag. The name must be unique. |
| `category` | string | yes | Category for the tag. |
| `description` | string | yes | Description for the tag. |
| `displays_on_dash` | boolean | yes | Display the tag under the associated patient photo block when the patient chart or encounter note is opened. |
| `note_displays_on_dashboard` | boolean | yes | Display the full text of any associated tag note in addition to showing the existence of the tag on the dashboard. This behavior is dependent on `displays_on_dash` being `true` as well. |
| `displays_on_calendar` | boolean | yes | Display in the scheduler interface when scheduling an appointment for a tagged patient. |
| `color` | string | yes | A valid six-digit hex code that defines the color for the tag. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `PATCH /tags/:tag_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag.md) for the provider-specific parameters and requirements.

