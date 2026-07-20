# FuseDesk: Search Emails

Finds emails in FuseDesk by matching search filters.

```
GET https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/search-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/search-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/search-emails?${params}`, {
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
| `bodyLimit` | number | no | Maximum email body length to return. |
| `content` | string | no | Search text in the email body. |
| `from` | string | no | Sender email address to match. |
| `limit` | number | no | Maximum number of emails to return. |
| `offset` | number | no | Number of emails to skip. |
| `orderBy` | string | no | Sort order expression. |
| `subject` | string | no | Search text in the email subject. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FuseDesk API returns.

## Native endpoint

Through the native FuseDesk API, this operation is `GET /api/v1/emails/unassigned` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-emails.md) for the provider-specific parameters and requirements.

