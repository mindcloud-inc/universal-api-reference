# Maildrip: Remove contacts from a group or delete them entirely (asynchronous).



```
DELETE https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/remove-contacts-from-a-group-or-delete-them-entirely-asynchronous
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/remove-contacts-from-a-group-or-delete-them-entirely-asynchronous?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/remove-contacts-from-a-group-or-delete-them-entirely-asynchronous?${params}`, {
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
| `groupId` | string | no | ID of the group from which contacts will be removed. Optional if contacts array is provided. Required if resetGroup is true. |
| `contacts[]` | array<string> | no | Array of contact IDs to remove or delete. Optional if groupId with resetGroup true is provided. Required otherwise. Accepts multiple values as an array. |
| `resetGroup` | boolean | no | If true, removes all contacts from the group (requires groupId). If false, removes only specified contacts from the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `PUT /api/v1/contacts/delete` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contacts-from-a-group-or-delete-them-entirely-asynchronous.md) for the provider-specific parameters and requirements.

