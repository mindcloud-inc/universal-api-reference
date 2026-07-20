# BigMailer: Delete Field

Deletes a field from a BigMailer brand.

```
DELETE https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/delete-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigMailer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/delete-field?connectionId=$CONNECTION_ID&brandId=string&fieldId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "brandId": "string",
  "fieldId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/delete-field?${params}`, {
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
| `brandId` | string | yes | ID of the brand containing the field. |
| `fieldId` | string | yes | ID of the field. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigMailer API returns.

## Native endpoint

Through the native BigMailer API, this operation is `DELETE /brands/:brand_id/fields/:field_id` (base URL `https://api.bigmailer.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-field.md) for the provider-specific parameters and requirements.

