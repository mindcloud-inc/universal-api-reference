# Watbot: Detach Tag From Contact

Detaches a tag from a contact in Watbot.

```
DELETE https://connect.mindcloud.co/v1/universal/watbot/latest/actions/detach-tag-from-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/detach-tag-from-contact?connectionId=$CONNECTION_ID&contactId=1&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1",
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watbot/latest/actions/detach-tag-from-contact?${params}`, {
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
| `contactId` | number | yes | ID контакта. |
| `name` | string | yes | Имя тега. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Watbot API returns.

## Native endpoint

Through the native Watbot API, this operation is `POST /detachTagFromContact` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detach-tag-from-contact.md) for the provider-specific parameters and requirements.

