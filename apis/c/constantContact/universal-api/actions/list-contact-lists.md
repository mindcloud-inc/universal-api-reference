# Constant Contact: List Contact Lists

Retrieves contact lists from Constant Contact.

```
GET https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-contact-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-contact-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-contact-lists?${params}`, {
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
| `includeCount` | boolean | no | Include total number of matching contact lists. |
| `includeMembershipCount` | string | no | Include list membership totals (`active` or `all`). |
| `name` | string | no | Filter by exact contact list name. |
| `status` | string | no | Filter by list status. |
| `channelType` | string | no | Filter by channel type (`email` or `sms`). |
| `includeSmsMembershipCount` | boolean | no | Include SMS member totals when channel type is `sms`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": {},
      "lists": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links` | object | Pagination links when present. |
| `lists` | array<object> | Collection of contact list resources. |

## Native endpoint

Through the native Constant Contact API, this operation is `GET /contact_lists` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-lists.md) for the provider-specific parameters and requirements.

