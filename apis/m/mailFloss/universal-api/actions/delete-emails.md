# MailFloss: Delete Emails

Deletes email addresses from MailFloss privacy storage.

```
DELETE https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/delete-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailFloss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/delete-emails?connectionId=$CONNECTION_ID&emails%5B%5D=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emails[]": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/delete-emails?${params}`, {
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
| `emails[]` | array<string> | yes | Email addresses to delete from MailFloss data privacy storage. |

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
| `status` | string | Success status for the delete request. |

## Native endpoint

Through the native MailFloss API, this operation is `POST /delete` (base URL `https://api.mailfloss.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-emails.md) for the provider-specific parameters and requirements.

