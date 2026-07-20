# Watbot: List Contact Referrers

Retrieves referrers for a Watbot contact.

```
GET https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-contact-referrers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-contact-referrers?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-contact-referrers?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `depth` | number | no | Глубина дерева от 1 до 10. |
| `isFlat` | boolean | no | 1 — вернуть плоский список вместо дерева. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Watbot API returns.

## Native endpoint

Through the native Watbot API, this operation is `GET /getReferrers` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-referrers.md) for the provider-specific parameters and requirements.

