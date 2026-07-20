# TravelPerk: Update SCIM User

Updates an existing SCIM user in TravelPerk.

```
PUT https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/update-scim-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TravelPerk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/update-scim-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scimUserId": "string",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/update-scim-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scimUserId": "string",
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scimUserId` | string | yes | The SCIM user identifier to update. |
| `firstName` | string | yes | The user's given name. |
| `lastName` | string | yes | The user's family name. |
| `email` | string | yes | The work email address used as the SCIM username. |
| `active` | boolean | no | Whether the user should be active in TravelPerk. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "externalId": "string",
      "groups": [
        {}
      ],
      "id": "string",
      "locale": "string",
      "meta": {},
      "name": {},
      "phoneNumbers": [
        {}
      ],
      "preferredLanguage": "string",
      "schemas": [
        "string"
      ],
      "title": "string",
      "urn:ietf:params:scim:schemas:extension:enterprise:2": {
        "0:User": {}
      },
      "urn:ietf:params:scim:schemas:extension:travelperk:2": {
        "0:User": {}
      },
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `externalId` | string |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `locale` | string |  |
| `meta` | object |  |
| `name` | object |  |
| `phoneNumbers` | array<object> |  |
| `preferredLanguage` | string |  |
| `schemas` | array<string> |  |
| `title` | string |  |
| `urn:ietf:params:scim:schemas:extension:enterprise:2.0:User` | object |  |
| `urn:ietf:params:scim:schemas:extension:travelperk:2.0:User` | object |  |
| `userName` | string |  |

## Native endpoint

Through the native TravelPerk API, this operation is `PUT https://app.sandbox-travelperk.com/api/v2/scim/Users/:scimUserId` (base URL `https://api.sandbox-travelperk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-scim-user.md) for the provider-specific parameters and requirements.

