# Formilla: Create or Update Contact (User ID Required)

Creates or updates a contact in Formilla by user ID.

```
POST https://connect.mindcloud.co/v1/universal/formilla/latest/actions/upsert-contact-by-user-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formilla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formilla/latest/actions/upsert-contact-by-user-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "user-123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formilla/latest/actions/upsert-contact-by-user-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "user-123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | A unique identifier for the contact. Example: `user-123`. |
| `email` | string | no | The contact's email address. Example: `customer@example.com`. |
| `firstName` | string | no | Example: `Taylor`. |
| `lastName` | string | no | Example: `Morgan`. |
| `phone` | string | no | Example: `+1 555 123 4567`. |
| `signedUpDate` | number | no | Unix timestamp for when the contact signed up. Example: `1704067200`. |
| `isUnsubscribed` | boolean | no |  |
| `customAttributes` | object | no | JSON object with custom contact key/value pairs. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Formilla API returns.

## Native endpoint

Through the native Formilla API, this operation is `POST /contacts` (base URL `https://api.formilla.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-contact-by-user-id.md) for the provider-specific parameters and requirements.

