# Dynosend: Create Contact and Ignore Double Opt-In

Creates a new contact in Dynosend without double opt-in.

```
POST https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/create-contact-ignore-double-opt-in
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/create-contact-ignore-double-opt-in" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audienceUid": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/create-contact-ignore-double-opt-in', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audienceUid": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audienceUid` | string | yes | The UID of the audience where the contact will be created. |
| `email` | string | yes | The email address of the contact to create. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dynosend API returns.

## Native endpoint

Through the native Dynosend API, this operation is `POST /contacts` (base URL `https://api.dynosend.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-ignore-double-opt-in.md) for the provider-specific parameters and requirements.

