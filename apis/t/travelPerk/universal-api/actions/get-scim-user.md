# TravelPerk: Get SCIM User

Retrieves a SCIM user from TravelPerk.

```
GET https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-scim-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TravelPerk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-scim-user?connectionId=$CONNECTION_ID&scimUserId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scimUserId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-scim-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scimUserId` | string | yes | The SCIM user identifier. |

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

Through the native TravelPerk API, this operation is `GET https://app.sandbox-travelperk.com/api/v2/scim/Users/:scimUserId` (base URL `https://api.sandbox-travelperk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scim-user.md) for the provider-specific parameters and requirements.

