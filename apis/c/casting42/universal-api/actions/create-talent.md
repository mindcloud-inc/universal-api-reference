# Casting42: Create Talent

Creates a new talent in Casting42.

```
POST https://connect.mindcloud.co/v1/universal/casting42/latest/actions/create-talent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Casting42 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/casting42/latest/actions/create-talent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/casting42/latest/actions/create-talent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | First name of the talent. |
| `lastName` | string | yes | Last name of the talent. |
| `email` | string | no | Email address of the talent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "age": 1,
      "birthday": "string",
      "createdAt": "string",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "hiddenName": "Ava Chen",
      "id": "string",
      "lastName": "Chen",
      "mobilePhone": "string",
      "profilePicture": "string",
      "skills": {},
      "slug": "string",
      "stageName": "Ava Chen",
      "tag": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | number | Talent age. |
| `birthday` | string | Talent birthday as returned by Casting42. |
| `createdAt` | string | Talent creation date as returned by Casting42. |
| `customFields` | array<object> | Custom field values returned for the talent. |
| `email` | string | Talent email address. |
| `firstName` | string | Talent first name. |
| `fullName` | string | Full talent name. |
| `hiddenName` | string | Privacy-safe display name. |
| `id` | string | Unique talent ID. |
| `lastName` | string | Talent last name. |
| `mobilePhone` | string | Talent mobile phone number. |
| `profilePicture` | string | Profile picture URL. |
| `skills` | object | Skill groups keyed by Casting42 field labels. |
| `slug` | string | Talent slug. |
| `stageName` | string | Talent stage name. |
| `tag` | string | Talent tag used across Casting42 endpoints. |
| `updatedAt` | string | Talent update date as returned by Casting42. |

## Native endpoint

Through the native Casting42 API, this operation is `POST /api/v2/talents` (base URL `https://casting42.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-talent.md) for the provider-specific parameters and requirements.

