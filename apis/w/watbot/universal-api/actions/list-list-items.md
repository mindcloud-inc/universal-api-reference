# Watbot: List List Items

Retrieves list items from a Watbot list schema.

```
GET https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-list-items?connectionId=$CONNECTION_ID&schemaId=5dee4800c2cc5a38ec797235" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schemaId": "5dee4800c2cc5a38ec797235"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-list-items?${params}`, {
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
| `schemaId` | string | yes | ID of the list schema. Example: `5dee4800c2cc5a38ec797235`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | number | no | Bot ID if the schema has a bot field. |
| `contactId` | number | no | Contact ID if the schema has a contact field. |
| `orderBy` | string | no | Sort field or field,direction expression. Example: `created_at,desc`. |
| `filters` | object | no | Filter object for list item fields. Example: `[object Object]`. |
| `page` | object | no | Page selection payload. Example: `[object Object]`. |
| `limit` | number | no | Maximum number of items to return. Example: `100`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Watbot API returns.

## Native endpoint

Through the native Watbot API, this operation is `POST /getListItems` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-list-items.md) for the provider-specific parameters and requirements.

