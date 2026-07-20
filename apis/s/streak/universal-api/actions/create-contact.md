# Streak: Create Contact

Creates a new contact in Streak.

```
POST https://connect.mindcloud.co/v1/universal/streak/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streak/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamKey": "string",
  "emailAddresses": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streak/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamKey": "string",
    "emailAddresses": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamKey` | string | yes | Team key. |
| `emailAddresses` | string<string> | yes | Email addresses to associate with the contact. Accepts multiple values as an array. |
| `getIfExisting` | boolean | no | If true, return an existing contact when the email already exists. |
| `givenName` | string | no | First name. |
| `familyName` | string | no | Last name. |
| `title` | string | no | Contact title or description. |
| `other` | string | no | Notes or other uncategorized information. |
| `addresses` | string<string> | no | Addresses to associate with the contact. Accepts multiple values as an array. |
| `phoneNumbers` | string<string> | no | Phone numbers to associate with the contact. Accepts multiple values as an array. |
| `twitterHandle` | string | no | Twitter handle. |
| `facebookHandle` | string | no | Facebook handle. |
| `linkedinHandle` | string | no | LinkedIn handle. |
| `photoUrl` | string | no | Photo URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        "string"
      ],
      "creationDate": "2026-05-07T12:00:00.000Z",
      "creatorKey": "string",
      "emailAddresses": [
        "ava@example.com"
      ],
      "familyName": "Ava Chen",
      "fields": {},
      "givenName": "Ava Chen",
      "key": "string",
      "lastEnrichmentTimestamp": "2026-05-07T12:00:00.000Z",
      "lastSavedTimestamp": "2026-05-07T12:00:00.000Z",
      "lastSavedUserKey": "string",
      "other": "string",
      "phoneNumbers": [
        "string"
      ],
      "teamKey": "string",
      "versionTimestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<string> | The contact addresses. |
| `creationDate` | date | When the contact was created. |
| `creatorKey` | string | The user who created the contact. |
| `emailAddresses` | array<string> | The contact email addresses. |
| `familyName` | string | The contact's last name. |
| `fields` | object | Custom field values keyed by field ID. |
| `givenName` | string | The contact's first name. |
| `key` | string | The contact key. |
| `lastEnrichmentTimestamp` | date | When the contact was last enriched. |
| `lastSavedTimestamp` | date | When the contact was last saved. |
| `lastSavedUserKey` | string | The user who last saved the contact. |
| `other` | string | Additional notes stored on the contact. |
| `phoneNumbers` | array<string> | The contact phone numbers. |
| `teamKey` | string | The team the contact belongs to. |
| `versionTimestamp` | date | When the current contact version was written. |

## Native endpoint

Through the native Streak API, this operation is `POST /api/v2/teams/:teamKey/contacts/` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

