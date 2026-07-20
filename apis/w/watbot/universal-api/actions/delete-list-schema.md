# Watbot: Delete List Schema

Deletes an existing list schema from Watbot.

```
DELETE https://connect.mindcloud.co/v1/universal/watbot/latest/actions/delete-list-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/delete-list-schema?connectionId=$CONNECTION_ID&schemaId=5dee4800c2cc5a38ec797235" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schemaId": "5dee4800c2cc5a38ec797235"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watbot/latest/actions/delete-list-schema?${params}`, {
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

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Watbot API returns.

## Native endpoint

Through the native Watbot API, this operation is `POST /deleteListSchema` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-list-schema.md) for the provider-specific parameters and requirements.

