# BigMailer: List Fields

Retrieves fields from a BigMailer brand.

```
GET https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigMailer `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/list-fields?connectionId=$CONNECTION_ID&limit=25&offset=0&brandId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "brandId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/list-fields?${params}`, {
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
| `brandId` | string | yes | ID of the brand whose fields should be returned. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigMailer API returns.

## Native endpoint

Through the native BigMailer API, this operation is `GET /brands/:brand_id/fields` (base URL `https://api.bigmailer.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

