# HubSpot: List Custom Object Records



```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-custom-object-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-custom-object-records?connectionId=$CONNECTION_ID&limit=25&offset=0&objectTypeId=2-123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "objectTypeId": "2-123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-custom-object-records?${params}`, {
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
| `objectTypeId` | string | yes | The custom object type ID from this HubSpot account, such as 2-123456. Use the object type ID, not its display label or a record ID. Example: `2-123456`. |
| `properties` | string<string> | no | Comma-separated internal property names to include in each record. Include the fields needed by your report. Example: `hs_object_id,hs_createdate`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertiesWithHistory` | string<string> | no | Comma-separated internal property names to return with their current and historical values. Example: `hs_lastmodifieddate`. |
| `associations` | string<string> | no | Comma-separated object types whose associated record IDs should be included. Example: `contacts,companies`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "associations": {},
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
| `archived` | boolean | Whether the record is archived. |
| `associations` | object | Associated record IDs grouped by requested object type. Included when requested. |
| `createdAt` | date | Record creation timestamp. |
| `id` | string | HubSpot record ID. |
| `properties` | object | Requested custom object properties. Keys vary with the object type and selected properties. |
| `propertiesWithHistory` | object | Requested property histories, keyed by property name. Included when requested. |
| `updatedAt` | date | Record last-update timestamp. |
| `url` | string | URL of this record in HubSpot. |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/v3/objects/:objectTypeId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-custom-object-records.md) for the provider-specific parameters and requirements.

