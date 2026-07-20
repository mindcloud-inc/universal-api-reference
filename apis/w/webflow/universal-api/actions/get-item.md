# Webflow: Get Item

Retrieves a staged collection item from Webflow.

```
GET https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-item?connectionId=$CONNECTION_ID&collectionId=string&itemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string",
  "itemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-item?${params}`, {
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
| `collectionId` | string | yes | The unique identifier of the collection. |
| `itemId` | string | yes | The unique identifier of the item. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cmsLocaleId` | string | no | Locale identifier for the returned item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cmsLocaleId": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "fieldData": {},
      "id": "string",
      "isArchived": true,
      "isDraft": true,
      "lastPublished": "2026-05-07T12:00:00.000Z",
      "lastUpdated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cmsLocaleId` | string | CMS locale ID. |
| `createdOn` | date | Creation timestamp. |
| `fieldData` | object | Collection item field values. |
| `id` | string | Item ID. |
| `isArchived` | boolean | Whether the item is archived. |
| `isDraft` | boolean | Whether the item is a draft. |
| `lastPublished` | date | Last published timestamp. |
| `lastUpdated` | date | Last updated timestamp. |

## Native endpoint

Through the native Webflow API, this operation is `GET /collections/:collection_id/items/:item_id` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

