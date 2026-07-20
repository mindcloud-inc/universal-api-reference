# SureCart: Delete Price



```
DELETE https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/delete-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/delete-price?connectionId=$CONNECTION_ID&id=08f7b8e3-7114-4a9b-b40e-f6fdf52a4fb4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "08f7b8e3-7114-4a9b-b40e-f6fdf52a4fb4"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/delete-price?${params}`, {
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
| `id` | string | yes | The price ID to delete. Example: `08f7b8e3-7114-4a9b-b40e-f6fdf52a4fb4`. |

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
| `deleted` | boolean |  |
| `id` | string |  |
| `object` | string |  |

## Native endpoint

Through the native SureCart API, this operation is `DELETE v1/prices/:id` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-price.md) for the provider-specific parameters and requirements.

