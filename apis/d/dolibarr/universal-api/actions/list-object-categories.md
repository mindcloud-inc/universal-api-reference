# Dolibarr: List Object Categories

Retrieves categories for an object in Dolibarr.

```
GET https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/list-object-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dolibarr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/list-object-categories?connectionId=$CONNECTION_ID&id=1&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/list-object-categories?${params}`, {
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
| `id` | number | yes | Dolibarr object ID associated with the category. |
| `type` | string | yes | Dolibarr object type associated with the category. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dolibarr API returns.

## Native endpoint

Through the native Dolibarr API, this operation is `GET /categories/object/{type}/{id}` (base URL `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-object-categories.md) for the provider-specific parameters and requirements.

