# HubSpot: Search Lists

Finds lists in HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-lists?${params}`, {
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
| `query` | string | no | Free-text query for list search. |
| `processingTypes[]` | array<string> | no | Optional list processing types filter. |
| `listIds[]` | array<string> | no | Optional list IDs filter. |
| `offset` | number | no | Pagination offset. |
| `count` | number | no | Page size. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalProperties": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdById": "string",
      "filtersUpdatedAt": "2026-05-07T12:00:00.000Z",
      "listId": "string",
      "listVersion": 1,
      "name": "Ava Chen",
      "objectTypeId": "string",
      "processingStatus": "string",
      "processingType": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedById": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalProperties` | object | Additional list metadata returned by HubSpot. |
| `createdAt` | date | When the list was created. |
| `createdById` | string | The creator user ID, when available. |
| `filtersUpdatedAt` | date | When the list filters were last updated. |
| `listId` | string | The list ID. |
| `listVersion` | number | The list version number. |
| `name` | string | The list name. |
| `objectTypeId` | string | The HubSpot object type ID tracked by the list. |
| `processingStatus` | string | The current list processing status. |
| `processingType` | string | The list processing type. |
| `updatedAt` | date | When the list was last updated. |
| `updatedById` | string | The updater user ID, when available. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/lists/search` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-lists.md) for the provider-specific parameters and requirements.

