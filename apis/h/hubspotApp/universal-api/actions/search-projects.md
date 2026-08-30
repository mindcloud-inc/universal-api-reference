# HubSpot: Search Projects



```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-projects?${params}`, {
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
| `filterGroups[].filters[]` | array<object> | no |  |
| `filterGroups[].filters[].propertyName` | string | no |  |
| `filterGroups[].filters[].operator` | string | no |  |
| `filterGroups[].filters[].value` | string | no |  |
| `properties[]` | array<string> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterGroups[].filters[].values[]` | array<string> | no |  |
| `filterGroups[].filters[].highValue` | string | no |  |
| `after` | string | no |  |
| `limit` | number | no |  |
| `sorts[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "propertiesWithHistory": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the project is archived. |
| `archivedAt` | date | When the project was archived. |
| `createdAt` | date | When the project was created. |
| `id` | string | HubSpot project record ID. |
| `properties` | object | Project property values returned by HubSpot. |
| `propertiesWithHistory` | object | Requested project property history. |
| `updatedAt` | date | When the project was last updated. |
| `url` | string | HubSpot project record URL. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/objects/2026-03/projects/search` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-projects.md) for the provider-specific parameters and requirements.

