# Raklet: Add Contact Email



```
POST https://connect.mindcloud.co/v1/universal/raklet/latest/actions/add-contact-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/add-contact-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organisationMembershipId": "string",
  "emailAddress": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raklet/latest/actions/add-contact-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organisationMembershipId": "string",
    "emailAddress": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organisationMembershipId` | string | yes | Contact membership identifier in Raklet. |
| `emailAddress` | string | yes | Email address to attach to the contact. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Raklet API returns.

## Native endpoint

Through the native Raklet API, this operation is `POST /organisations/:organisationId/contacts/:organisationMembershipId/emails` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-email.md) for the provider-specific parameters and requirements.

