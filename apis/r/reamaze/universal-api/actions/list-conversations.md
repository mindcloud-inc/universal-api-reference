# Reamaze: List Conversations



```
GET https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-conversations?${params}`, {
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
| `filter` | string | no | Conversation scope filter. Supported values include archived, open, unassigned, or all. |
| `archived` | string | no | `filter` with `archived`, `open`, `unassigned`, or `all` will show only Archived, Open, Unassigned or All conversations, respectively. |
| `open` | string | no | `filter` with `archived`, `open`, `unassigned`, or `all` will show only Archived, Open, Unassigned or All conversations, respectively. |
| `unassigned` | string | no | `filter` with `archived`, `open`, `unassigned`, or `all` will show only Archived, Open, Unassigned or All conversations, respectively. |
| `all` | string | no | `filter` with `archived`, `open`, `unassigned`, or `all` will show only Archived, Open, Unassigned or All conversations, respectively. |
| `forEmail` | string | no | Return only conversations relevant to the given user email. |
| `email` | string | no | `for` with a value matching a known user `email` will return only conversations relevant to that user. For example, for a customer user, this would be conversations visible to that customer. |
| `forId` | string | no | Return only conversations relevant to the given customer SSO ID. |
| `id` | string | no | `for_id` with a value matching a known user `id` (from SSO) will return only conversations relevant to that customer user. |
| `sort` | string | no | Supported values include updated or changed. |
| `updated` | date | no | `sort` with a value of `updated` will return conversations in descending order of last customer update. A value of `changed` will return conversations in descending order of any update or status change. The default sort order is by conversation `create_at`. |
| `tag` | string | no | Comma-separated conversation tags to match. |
| `category` | string | no | Return only conversations from the given channel slug. |
| `dataKeyValue` | string | no | `data` with a hash of key/value pairs (e.g. `data[key]=value`) will return conversations with `data` matching those key/value pairs. |
| `startDate` | date | no | Filter by latest customer message on or after this ISO 8601 date-time. |
| `endDate` | date | no | Filter by latest customer message on or before this ISO 8601 date-time. |
| `origin` | string | no | Filter by conversation origin, for example email, chat, api, instagram, sms, voice, custom, staff, or form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversations": [
        {}
      ],
      "pageCount": 1,
      "pageSize": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversations` | array<object> |  |
| `pageCount` | number |  |
| `pageSize` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Reamaze API, this operation is `GET /conversations` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

