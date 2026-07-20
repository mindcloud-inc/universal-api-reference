# Leadfox: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/leadfox/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadfox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leadfox/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "person@example.com",
  "lifecycle": "lead"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadfox/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "person@example.com",
    "lifecycle": "lead"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Contact email address (mandatory). Example: `person@example.com`. |
| `lifecycle` | string | yes | Contact lifecycle stage. Allowed values: subscriber, lead, mql, sql, customer. Example: `lead`. |
| `firstname` | string | no | Contact first name. Example: `Ada`. |
| `lastname` | string | no | Contact last name. Example: `Lovelace`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadfox API returns.

## Native endpoint

Through the native Leadfox API, this operation is `POST /contact/save/` (base URL `https://app.leadfox.co/service`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

