# MailSlurp Email Plugin: Delete Email

Deletes an existing email from MailSlurp.

```
DELETE https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/delete-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailSlurp Email Plugin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/delete-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/delete-email?${params}`, {
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
| `emailId` | string | no | The MailSlurp email ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native MailSlurp Email Plugin API, this operation is `DELETE /emails/:emailId` (base URL `https://api.mailslurp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-email.md) for the provider-specific parameters and requirements.

