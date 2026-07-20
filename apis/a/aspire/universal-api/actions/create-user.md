# Aspire: Create User

Retrieves pay codes from your Aspire account.

```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "active": "False",
  "allBranchAccess": "False",
  "externalContactReference": "string",
  "password": "string",
  "UserRoles[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "active": "False",
    "allBranchAccess": "False",
    "externalContactReference": "string",
    "password": "string",
    "UserRoles[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | boolean | yes | Default: `False`. |
| `allBranchAccess` | boolean | yes | Default: `False`. |
| `BranchAccess[]` | array<number> | no |  |
| `externalContactReference` | list<string> | yes |  |
| `password` | string | yes |  |
| `UserRoles[]` | array<number> | yes |  |
| `VerifyPassword` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `POST Users` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

