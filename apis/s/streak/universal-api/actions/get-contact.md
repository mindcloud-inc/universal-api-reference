# Streak: Get Contact

Retrieves a contact from Streak.

```
GET https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-contact?${params}`, {
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
| `contactKey` | string | yes | Contact key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        "string"
      ],
      "contactLinks": [
        {}
      ],
      "creationDate": "2026-05-07T12:00:00.000Z",
      "creatorKey": "string",
      "domains": [
        "string"
      ],
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
      "normalizedDomains": [
        "string"
      ],
      "orgLinks": [
        {}
      ],
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
| `contactLinks` | array<object> | Links from this contact to related contacts. |
| `creationDate` | date | When the contact was created. |
| `creatorKey` | string | The user who created the contact. |
| `domains` | array<string> | Domains associated with the contact. |
| `emailAddresses` | array<string> | The contact email addresses. |
| `familyName` | string | The contact's last name. |
| `fields` | object | Custom field values keyed by field ID. |
| `givenName` | string | The contact's first name. |
| `key` | string | The contact key. |
| `lastEnrichmentTimestamp` | date | When the contact was last enriched. |
| `lastSavedTimestamp` | date | When the contact was last saved. |
| `lastSavedUserKey` | string | The user who last saved the contact. |
| `normalizedDomains` | array<string> | Normalized domains associated with the contact. |
| `orgLinks` | array<object> | Links from this contact to related organizations. |
| `other` | string | Additional notes stored on the contact. |
| `phoneNumbers` | array<string> | The contact phone numbers. |
| `teamKey` | string | The team the contact belongs to. |
| `versionTimestamp` | date | When the current contact version was written. |

## Native endpoint

Through the native Streak API, this operation is `GET /api/v2/contacts/:contactKey` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

