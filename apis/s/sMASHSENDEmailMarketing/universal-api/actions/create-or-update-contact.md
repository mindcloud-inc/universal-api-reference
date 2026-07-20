# SMASHSEND Email Marketing: Create Or Update Contact

Creates or updates a contact in SMASHSEND by email.

```
POST https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/create-or-update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMASHSEND Email Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/create-or-update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/create-or-update-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "properties": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties` | object | yes | Contact properties payload wrapped under the documented properties object. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMASHSEND Email Marketing API returns.

## Native endpoint

Through the native SMASHSEND Email Marketing API, this operation is `POST /v1/contacts` (base URL `https://api.smashsend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-contact.md) for the provider-specific parameters and requirements.

