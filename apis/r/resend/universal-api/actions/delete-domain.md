# Resend: Delete Domain

Deletes an existing domain from Resend.

```
DELETE https://connect.mindcloud.co/v1/universal/resend/latest/actions/delete-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/resend/latest/actions/delete-domain?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resend/latest/actions/delete-domain?${params}`, {
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
| `id` | string<string> | yes | The Domain ID (UUID) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the domain was deleted. |
| `id` | string | Domain identifier. |
| `object` | string | Object type identifier. |

## Native endpoint

Through the native Resend API, this operation is `DELETE /domains/:id` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-domain.md) for the provider-specific parameters and requirements.

