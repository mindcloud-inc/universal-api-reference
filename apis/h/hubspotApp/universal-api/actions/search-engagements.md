# HubSpot: Search Engagements

Finds engagement records in HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-engagements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-engagements?connectionId=$CONNECTION_ID&engagementType=notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "engagementType": "notes"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-engagements?${params}`, {
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
| `engagementType` | list | yes | The CRM activity object type to search, such as notes, tasks, calls, emails, or meetings. One of: `calls`, `communications`, `emails`, `meetings`, `notes`, `postal_mail`, `tasks`. Example: `notes`. |
| `filterGroups` | object<object> | no | Use HubSpot filter groups to find activities linked to a record. For deal activity, use `associations.deal` with `EQ` and the deal ID. You can also use `associations.contact` or `associations.company`. |
| `filterGroups[].filters[]` | array<object> | no | Filters combined with AND semantics inside one filter group. For deal activity, add a filter using `associations.deal` and the deal ID. |
| `filterGroups[].filters[].propertyName` | string | no | HubSpot property to filter on. For related-record activity lookups, use `associations.deal`, `associations.contact`, or `associations.company`. Example: `associations.deal`. |
| `filterGroups[].filters[].operator` | list<string> | no | Comparison operator for the filter. `EQ` is the usual choice for association filters such as `associations.deal = <dealId>`. One of: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. Default: `EQ`. |
| `filterGroups[].filters[].value` | string | no | Single comparison value for the filter. For deal activity lookups, pass the deal ID such as `9018868490`. Example: `9018868490`. |
| `properties[]` | array<string> | no | Properties to return for each activity. For deal emails, try `hs_email_subject`, `hs_email_text`, `hs_email_from_email`, `hs_email_to_email`, and `hs_timestamp`. For deal notes, try `hs_note_body` and `hs_timestamp`. |
| `query` | string | no | Optional full-text query applied to the default searchable properties for the selected activity type. Example: `a`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of records to return in this search page. Example: `10`. |
| `after` | string | no | Paging cursor for the next search page. Example: `next-cursor`. |
| `sorts[]` | array<string> | no | Sort clauses to apply to the search results. |
| `filterGroups[].filters[].values[]` | array<string> | no | Multiple comparison values for IN and NOT_IN filters. |
| `filterGroups[].filters[].highValue` | string | no | Upper bound value for BETWEEN filters. Example: `z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
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
| `archived` | boolean |  |
| `createdAt` | date |  |
| `id` | string |  |
| `properties` | object |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/:engagementType/search` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-engagements.md) for the provider-specific parameters and requirements.

