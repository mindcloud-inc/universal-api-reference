# Raisely: Upsert User

Finds a user in Raisely, or creates one if no match is found.

```
PUT https://connect.mindcloud.co/v1/universal/raisely/latest/actions/upsert-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/upsert-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaign": "string",
  "data.interaction.detail": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raisely/latest/actions/upsert-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaign": "string",
    "data.interaction.detail": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaign` | string | yes | The `uuid`, `path` or domain of the campaign to associate with the request |
| `data` | object | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.address1` | string | no | Line 1 of an address Example: `31 Sunset Boulevard` |
| `data.address2` | string | no | Line 2 of an address Example: `Unit 31b` |
| `data.adminSettings` | object | no | Object containing settings for admin users |
| `data.country` | string | no | The country of the user Examples: `AU`, `GB`, `US` |
| `data.email` | string | no | The user's email address. Raisely uses this as a unique identifier and will deduplicate on email. Example: `harveymilk@example.com` |
| `data.firstName` | string | no | The first name of the user Example: `Leila` |
| `data.fullName` | string | no | The full name of the user Example: `Leila Norma de Lima` |
| `data.isSamlLogin` | boolean | no | Will be true if this user logs in via organisation SAML login Examples: `true`, `false` |
| `data.language` | string | no | The language the user last interacted in |
| `data.lastName` | string | no | The last name of the user Example: `de Lima` |
| `data.phoneNumber` | string | no | Phone number of the user Example: `+1 123-456-7890` |
| `data.photoUrl` | string | no | URL of the user's photo Example: `https://raisely-images.imgix.net/www/uploads/t-03-arl-8-es-uhhqua-4-pr-f-4865431-df-58-512-png-08e3f5.png` |
| `data.postcode` | string | no | Postal code of the user Examples: `AAA BBBB`, `0000`, `AAA BBB` |
| `data.preferredName` | string | no | The name that the user prefers to be called Example: `Norma` |
| `data.state` | string | no | The state/province of the user Examples: `Victoria`, `New York`, `British Columbia` |
| `data.suburb` | string | no | The suburb/city of the user Examples: `Melbourne`, `Albany`, `Vancouver` |
| `data.swiftAidAuthExpiry` | string | no | Date of expiry of donor authorisation for SwiftAid |
| `data.tags[]` | array<string> | no | Tag UUIDs or paths to assign to the user |
| `data.interaction` | object | no | The interaction to create assigned to this user |
| `data.interaction.categoryUuid` | string | no | The category UUID of the interaction to create |
| `data.interaction.detail` | object | yes | Additional details relating to this Raisely interaction |
| `data.interaction.detail.comment` | string | no |  |
| `data.interaction.detail.pinned` | boolean | no |  |
| `data.interaction.detail.private` | object | no |  |
| `data.interaction.detail.public` | object | no |  |
| `data.interaction.detail.readOnly` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "organisationUuid": "string",
      "permission": "string",
      "phoneNumber": "string",
      "photoUrl": "https://example.com",
      "preferredName": "Ava Chen",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `organisationUuid` | string |  |
| `permission` | string |  |
| `phoneNumber` | string |  |
| `photoUrl` | string |  |
| `preferredName` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Raisely API, this operation is `POST /users/upsert` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-user.md) for the provider-specific parameters and requirements.

