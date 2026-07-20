# Datalyse: Get Emails

Retrieves emails from Datalyse by folder.

```
GET https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/get-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datalyse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/get-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/get-emails?${params}`, {
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
| `page` | string | no | Page number Default: `1`. |
| `resultsPerPage` | string | no | Maximum number of results Default: `20`. |
| `searchValue` | string | no | Search in subject (optional) |
| `type` | string | no | Folder: "inbox" (default) or "sent" Default: `inbox`. |
| `unreadOnly` | string | no | Show only unread, set to "y" (optional) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | API response status |

## Native endpoint

Through the native Datalyse API, this operation is `POST /api/1.0/emails/get.json` (base URL `https://api.datalyse.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-emails.md) for the provider-specific parameters and requirements.

