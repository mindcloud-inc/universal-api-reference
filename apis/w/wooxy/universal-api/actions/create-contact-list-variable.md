# Wooxy: Create Contact List Variable

Creates a new contact list variable in Wooxy.

```
POST https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-contact-list-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-contact-list-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactListId": "yourContactListId",
  "variables[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-contact-list-variable', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactListId": "yourContactListId",
    "variables[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactListId` | string | yes | Wooxy contact list ID. Example: `yourContactListId`. |
| `variables[]` | array<object> | yes | Array of variable objects with required name and type (ENUM_STRING or ENUM_DATE). Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wooxy API returns.

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/contact-list/variables/add` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-list-variable.md) for the provider-specific parameters and requirements.

