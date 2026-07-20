# SendPulse: Delete Emails From Mailing List

Deletes subscribers from a SendPulse mailing list.

```
DELETE https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/delete-emails-from-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/delete-emails-from-mailing-list?connectionId=$CONNECTION_ID&mailingListId=123456&emails%5B%5D=user%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailingListId": "123456",
  "emails[]": "user@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/delete-emails-from-mailing-list?${params}`, {
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
| `mailingListId` | string | yes | The SendPulse mailing list identifier. Example: `123456`. |
| `emails[]` | array<string> | yes | Email addresses to remove from the mailing list. Example: `user@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean |  |

## Native endpoint

Through the native SendPulse API, this operation is `DELETE /addressbooks/:mailingListId/emails` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-emails-from-mailing-list.md) for the provider-specific parameters and requirements.

