# Productlane: Delete Doc Article

Deletes a help center article from Productlane.

```
DELETE https://connect.mindcloud.co/v1/universal/productlane/latest/actions/delete-doc-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/delete-doc-article?connectionId=$CONNECTION_ID&id=95697bff-03d3-4ca1-b079-a153436116ba" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "95697bff-03d3-4ca1-b079-a153436116ba"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productlane/latest/actions/delete-doc-article?${params}`, {
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
| `id` | string | yes | Doc article ID to delete. Example: `95697bff-03d3-4ca1-b079-a153436116ba`. |

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

Through the native Productlane API, this operation is `DELETE /docs/articles/{id}` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-doc-article.md) for the provider-specific parameters and requirements.

