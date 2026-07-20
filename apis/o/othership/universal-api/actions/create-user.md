# Othership: Create User

Creates a new user in Othership.

```
POST https://connect.mindcloud.co/v1/universal/othership/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Othership `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/othership/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/othership/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userName` | string | yes | The SCIM username, typically the user's work email. |
| `email` | string | no | The user's primary work email. |
| `displayName` | string | no | Display-friendly full name for the SCIM user. |
| `givenName` | string | no | The user's first name. |
| `familyName` | string | no | The user's last name. |
| `active` | boolean | no | Administrative status for the SCIM user. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | no | Provisioning-domain identifier used to correlate the user across systems. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "emails": [
        {
          "value": "ava@example.com"
        }
      ],
      "externalId": "string",
      "id": 1,
      "meta": {
        "resourceType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `emails[].value` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `meta.resourceType` | string |  |

## Native endpoint

Through the native Othership API, this operation is `POST /Users` (base URL `https://hwms-api.othership.com/api/v1/azure/scim`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

