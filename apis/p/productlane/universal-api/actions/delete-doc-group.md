# Productlane: Delete Doc Group

Deletes a doc group from your Productlane help center.

```
DELETE https://connect.mindcloud.co/v1/universal/productlane/latest/actions/delete-doc-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/delete-doc-group?connectionId=$CONNECTION_ID&id=a48ae618-61e4-4ec1-b23a-56ac476c95d5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "a48ae618-61e4-4ec1-b23a-56ac476c95d5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productlane/latest/actions/delete-doc-group?${params}`, {
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
| `id` | string | yes | Doc group ID to delete. Example: `a48ae618-61e4-4ec1-b23a-56ac476c95d5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isDeleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isDeleted` | boolean |  |

## Native endpoint

Through the native Productlane API, this operation is `DELETE /docs/groups/{id}` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-doc-group.md) for the provider-specific parameters and requirements.

