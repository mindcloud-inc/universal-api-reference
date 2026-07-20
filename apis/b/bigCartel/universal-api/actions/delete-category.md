# Big Cartel: Delete Category

Deletes a category from Big Cartel.

```
DELETE https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/delete-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Big Cartel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/delete-category?connectionId=$CONNECTION_ID&accountId=1&categoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "categoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/delete-category?${params}`, {
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
| `accountId` | number | yes | The Big Cartel account ID. |
| `categoryId` | string | yes | Category identifier from the categories endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native Big Cartel API, this operation is `DELETE /v1/accounts/[:account-id]/categories/[:category-id]` (base URL `https://api.bigcartel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-category.md) for the provider-specific parameters and requirements.

