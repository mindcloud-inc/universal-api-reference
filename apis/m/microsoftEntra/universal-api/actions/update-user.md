# Microsoft Entra: Update User



```
PUT https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Entra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "87d349ed-44d7-43e1-9a83-5f2406dee5bd"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "87d349ed-44d7-43e1-9a83-5f2406dee5bd"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `displayName` | string | no | Example: `Ava T.`. |
| `userId` | list<string> | yes | Example: `87d349ed-44d7-43e1-9a83-5f2406dee5bd`. |
| `givenName` | string | no | Example: `Ava`. |
| `surname` | string | no | Example: `Thompson`. |
| `jobTitle` | string | no | Example: `Operations Manager`. |
| `department` | string | no | Example: `Customer Success`. |
| `officeLocation` | string | no | Example: `Building A`. |
| `companyName` | string | no | Example: `Acme Logistics`. |
| `city` | string | no | Example: `San Francisco`. |
| `state` | string | no | Example: `California`. |
| `country` | string | no | Example: `United States`. |
| `streetAddress` | string | no | Example: `100 Market St`. |
| `postalCode` | string | no | Example: `94105`. |
| `preferredLanguage` | string | no | Example: `en-US`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Entra API returns.

## Native endpoint

Through the native Microsoft Entra API, this operation is `PATCH /users/:userId` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

