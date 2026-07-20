# Webflow: Create Collection

Creates a new collection in Webflow.

```
POST https://connect.mindcloud.co/v1/universal/webflow/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string",
  "displayName": "Ava Chen",
  "singularName": "Ava Chen",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webflow/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string",
    "displayName": "Ava Chen",
    "singularName": "Ava Chen",
    "slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | yes | The unique identifier of the site. |
| `displayName` | string | yes | Display name for the collection. |
| `singularName` | string | yes | Singular noun for the collection. |
| `slug` | string | yes | Slug for the collection. |
| `fields` | list<object> | no | List of collection field definitions. |

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

Through the native Webflow API, this operation is `POST /sites/:site_id/collections` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

