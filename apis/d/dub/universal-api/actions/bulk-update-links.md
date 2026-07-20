# Dub: Bulk Update Links

Updates links in Dub in bulk.

```
PUT https://connect.mindcloud.co/v1/universal/dub/latest/actions/bulk-update-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dub/latest/actions/bulk-update-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dub/latest/actions/bulk-update-links', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `linkIds[]` | array<string> | no | IDs of the links to update. Use this field or `External IDs` to choose the target links. |
| `data` | object | no | Fields in this section are applied to every selected link. |
| `externalIds[]` | array<string> | no | External IDs of the links to update. Use this field or `Target Link IDs` to choose the target links. |
| `data.url` | string | no | Updated destination URL applied to every selected link in this batch. |
| `data.title` | string | no | Updated title applied to every selected link in this batch. |
| `data.description` | string | no | Updated description applied to every selected link in this batch. |
| `data.archived` | boolean | no | Archive or unarchive every selected link. |
| `data.trackConversion` | boolean | no | Enable or disable conversion tracking for every selected link. |
| `data.tagIds[]` | array<string> | no | Tag IDs to assign to every selected link. |
| `data.tagNames[]` | array<string> | no | Tag names to assign to every selected link. |
| `data.folderId` | string | no | Folder ID to assign to every selected link. |
| `data.comments` | string | no | Comments applied to every selected link. |
| `data.expiresAt` | date | no | ISO-8601 expiration timestamp applied to every selected link. Example: `2026-06-01T12:00:00Z`. |
| `data.expiredUrl` | string | no | Destination URL to use after expiration for every selected link. Example: `https://example.com/expired`. |
| `data.publicStats` | boolean | no | Make stats public or private for every selected link. |
| `data.utmSource` | string | no | UTM source applied to every selected link. |
| `data.utmMedium` | string | no | UTM medium applied to every selected link. |
| `data.utmCampaign` | string | no | UTM campaign applied to every selected link. |
| `data.utmTerm` | string | no | UTM term applied to every selected link. |
| `data.utmContent` | string | no | UTM content applied to every selected link. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dub API returns.

## Native endpoint

Through the native Dub API, this operation is `PATCH /links/bulk` (base URL `https://api.dub.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-links.md) for the provider-specific parameters and requirements.

