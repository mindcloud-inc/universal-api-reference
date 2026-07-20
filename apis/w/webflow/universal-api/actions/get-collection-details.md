# Webflow: Get Collection Details

Retrieves details for a collection from Webflow.

```
GET https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-collection-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-collection-details?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-collection-details?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "fields": [
        {}
      ],
      "id": "string",
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "singularName": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date | Creation timestamp. |
| `displayName` | string | Display name for the collection. |
| `fields` | array<object> | Collection field definitions. |
| `id` | string | Collection ID. |
| `lastUpdated` | date | Last update timestamp. |
| `singularName` | string | Singular item name for the collection. |
| `slug` | string | Collection slug. |

## Native endpoint

Through the native Webflow API, this operation is `GET /collections/:collection_id` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection-details.md) for the provider-specific parameters and requirements.

