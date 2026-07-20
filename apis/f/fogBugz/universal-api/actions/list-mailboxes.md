# FogBugz: List Mailboxes

Retrieves mailboxes from FogBugz.

```
GET https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-mailboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FogBugz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-mailboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-mailboxes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "ixMailbox": 1,
      "sEmail": "ava@example.com",
      "sEmailUser": "ava@example.com",
      "sTemplate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ixMailbox` | number | Mailbox ID. |
| `sEmail` | string | Mailbox email address. |
| `sEmailUser` | string | Mailbox sender identity. |
| `sTemplate` | string | Mailbox email signature template. |

## Native endpoint

Through the native FogBugz API, this operation is `POST /listMailboxes` (base URL `{{credentials.siteUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mailboxes.md) for the provider-specific parameters and requirements.

