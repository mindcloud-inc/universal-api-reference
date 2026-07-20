# Routee: Unsubscribe contact from the defined mailing list

Unsubscribes a contact from a Routee mailing list.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/unsubscribe-contact-from-the-defined-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/unsubscribe-contact-from-the-defined-mailing-list?connectionId=$CONNECTION_ID&id=1&emails=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "emails": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/unsubscribe-contact-from-the-defined-mailing-list?${params}`, {
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
| `id` | number | yes | the ID of the mailing list |
| `emails` | string | yes | contact, which you want to unsubscribe from defined mailing list ["example@yourdomain.com"] |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `GET /addressbooks/:id/emails/unsubscribe` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-contact-from-the-defined-mailing-list.md) for the provider-specific parameters and requirements.

