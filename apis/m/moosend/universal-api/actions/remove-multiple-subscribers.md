# Moosend: Remove Multiple Subscribers

Deletes multiple subscribers from Moosend.

```
DELETE https://connect.mindcloud.co/v1/universal/moosend/latest/actions/remove-multiple-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/remove-multiple-subscribers?connectionId=$CONNECTION_ID&mailingListId=string&emails=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailingListId": "string",
  "emails": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moosend/latest/actions/remove-multiple-subscribers?${params}`, {
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
| `mailingListId` | string | yes | The ID of the email list that contains the subscribers you want to remove. |
| `emails` | object | yes | A list of subscriber email addresses that you want to remove from the email list. Use a comma (,) to separate the email addresses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailsIgnored": 1,
      "emailsProcessed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailsIgnored` | number |  |
| `emailsProcessed` | number |  |

## Native endpoint

Through the native Moosend API, this operation is `POST /subscribers/{{MailingListID}}/remove-many.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-multiple-subscribers.md) for the provider-specific parameters and requirements.

