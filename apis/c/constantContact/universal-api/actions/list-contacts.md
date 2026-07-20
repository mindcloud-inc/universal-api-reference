# Constant Contact: List Contacts

Retrieves contact records from Constant Contact.

```
GET https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-contacts?${params}`, {
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
| `email` | string | no | Search contacts by a specific email address. |
| `status` | string | no | Filter contacts by lifecycle status. |
| `lists` | string | no | Filter contacts by one or more contact list IDs. |
| `segmentId` | string | no | Return contacts that match a specific segment ID. |
| `tags` | string | no | Filter contacts by one or more tag IDs. |
| `updatedAfter` | date | no | Return contacts updated after this datetime (ISO-8601). |
| `updatedBefore` | date | no | Return contacts updated before this datetime (ISO-8601). |
| `createdAfter` | date | no | Return contacts created after this datetime (ISO-8601). |
| `createdBefore` | date | no | Return contacts created before this datetime (ISO-8601). |
| `optoutAfter` | date | no | Return contacts that opted out after this datetime (ISO-8601). |
| `optoutBefore` | date | no | Return contacts that opted out before this datetime (ISO-8601). |
| `include` | string | no | Include specific contact sub-resources in the response. |
| `smsStatus` | string | no | Filter contacts by SMS consent status. |
| `includeCount` | boolean | no | Include total matching contacts count in response metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {}
      ],
      "contactsCount": 1,
      "links": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | array<object> | Collection of contact resources. |
| `contactsCount` | number | Total number of contacts in the response when available. |
| `links` | object | Pagination links when present. |
| `status` | string | Processing status for segment-based queries when returned. |

## Native endpoint

Through the native Constant Contact API, this operation is `GET /contacts` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

