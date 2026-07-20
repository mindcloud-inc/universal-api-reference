# Vtiger CRM: Create Contact

Creates a new contact in Vtiger CRM.

```
POST https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vtiger CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "element": {
    "email": "oneshot.create.contact.action.20260320@mindcloud.co",
    "lastname": "Create Contact Action 2026-03-20",
    "firstname": "OneShot"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "element": {"email":"oneshot.create.contact.action.20260320@mindcloud.co","lastname":"Create Contact Action 2026-03-20","firstname":"OneShot"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `element` | string | yes | JSON object string for the Contact fields to create. Default: `{"email":"oneshot.create.contact.action.20260320@mindcloud.co","lastname":"Create Contact Action 2026-03-20","firstname":"OneShot"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "label": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Vtiger Contact id. |
| `label` | string | Contact label. |
| `url` | string | Contact URL in Vtiger. |

## Native endpoint

Through the native Vtiger CRM API, this operation is `POST /create?elementType=Contacts` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

