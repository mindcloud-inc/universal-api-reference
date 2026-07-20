# AMcards.com: Create Contact

Creates a new contact in AMcards.com.

```
POST https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AMcards.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groups[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groups[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addressLine1` | string | no | Primary street address for the contact. |
| `addressLine2` | string | no | Secondary address line for apartment, suite, or unit. |
| `birthDay` | string | no | Birth day value used for AMcards reminder/contact data. |
| `birthMonth` | string | no | Birth month value used for AMcards reminder/contact data. |
| `birthYear` | string | no | Birth year value used for AMcards reminder/contact data. |
| `city` | string | no | City for the contact mailing address. |
| `country` | string | no | Two-letter country code for the contact mailing address. |
| `emailAddress` | string | no | Email address for the contact. |
| `firstName` | string | no | First name for the contact. |
| `groups[]` | array<string> | yes | List of AMcards group resource URIs. Use an empty list when the contact should not be assigned to a group. |
| `lastName` | string | no | Last name for the contact. |
| `notes` | string | no | Freeform note stored on the AMcards contact. |
| `owner` | string | no | AMcards owner resource URI such as `/.api/v1/user/47054/`. |
| `phoneNumber` | string | no | Phone number for the contact. |
| `postalCode` | string | no | Postal code for the contact mailing address. |
| `state` | string | no | State or province for the contact mailing address. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AMcards.com API returns.

## Native endpoint

Through the native AMcards.com API, this operation is `POST /contact/` (base URL `https://amcards.com/.api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

