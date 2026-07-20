# Leadboxer: Create Or Associate User

Creates a user in Leadboxer, or associates an existing one.

```
POST https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/create-or-associate-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadboxer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/create-or-associate-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "userEmail": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen",
  "accountId": "string",
  "timezone": "string",
  "datasetIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/create-or-associate-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "userEmail": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen",
    "accountId": "string",
    "timezone": "string",
    "datasetIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes |  |
| `userEmail` | string | yes |  |
| `firstName` | string | yes |  |
| `lastName` | string | yes |  |
| `accountId` | string | yes |  |
| `timezone` | string | yes |  |
| `datasetIds[]` | array<string> | yes |  |
| `sendEmail` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadboxer API returns.

## Native endpoint

Through the native Leadboxer API, this operation is `POST /v1/users` (base URL `https://data.leadboxer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-associate-user.md) for the provider-specific parameters and requirements.

