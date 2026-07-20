# Podio: Delete Item

Deletes an existing item from Podio.

```
DELETE https://connect.mindcloud.co/v1/universal/podio/latest/actions/delete-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/podio/latest/actions/delete-item?connectionId=$CONNECTION_ID&itemId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/delete-item?${params}`, {
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
| `itemId` | number | yes | The id of the item. Example: `123456789`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hook` | boolean | no | True to run item hooks. |
| `silent` | boolean | no | True to suppress notifications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Empty response body on success. |

## Native endpoint

Through the native Podio API, this operation is `DELETE /item/:item_id` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-item.md) for the provider-specific parameters and requirements.

