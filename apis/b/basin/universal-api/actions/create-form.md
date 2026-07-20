# Basin: Create Form

Creates a new form in Basin.

```
POST https://connect.mindcloud.co/v1/universal/basin/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/basin/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/basin/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "form.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `form` | object | no | Form fields to create. |
| `form.name` | string | yes | Form name. |
| `form.project_id` | number | no | Project ID for the new form. |
| `form.timezone` | string | no | Form timezone. |
| `form.redirect_url` | string | no | Redirect URL after submission. |
| `form.notification_emails` | string | no | Notification recipient emails. |
| `form.autoreply` | boolean | no | Whether autoreply is enabled. |
| `form.autoreply_body` | string | no | Autoresponse email body. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basin API returns.

## Native endpoint

Through the native Basin API, this operation is `POST /api/v1/forms/` (base URL `https://usebasin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

