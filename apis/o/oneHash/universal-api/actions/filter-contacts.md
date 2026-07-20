# OneHash: Filter Contacts

Finds contacts in OneHash using filters.

```
GET https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/filter-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneHash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/filter-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/filter-contacts?${params}`, {
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
| `accountId` | string | no | OneHash Chat account id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneHash API returns.

## Native endpoint

Through the native OneHash API, this operation is `POST /api/v1/accounts/:accountId/contacts/filter` (base URL `https://chat.onehash.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-contacts.md) for the provider-specific parameters and requirements.

