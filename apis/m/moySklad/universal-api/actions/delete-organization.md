# MoySklad: Delete organization

Deletes an organization from MoySklad.

```
DELETE https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/delete-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/delete-organization?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/delete-organization?${params}`, {
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
| `id` | string | yes | MoySklad organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `meta` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native MoySklad API, this operation is `DELETE entity/organization/:id` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-organization.md) for the provider-specific parameters and requirements.

