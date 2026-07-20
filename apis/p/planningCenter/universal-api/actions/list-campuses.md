# Planning Center: List Campuses

Retrieves campuses from Planning Center.

```
GET https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-campuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planning Center `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-campuses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-campuses?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Include associated resources Example: `lists,service_times`. |
| `order` | string | no | Sort returned campuses Example: `-updated_at`. |
| `where` | object | no | Equality filters for campus fields |
| `where.createdAt` | date | no | Query on a specific created_at Example: `2000-01-01T12:00:00Z`. |
| `where.id` | number | no | Query on a specific id Example: `12345`. |
| `where.updatedAt` | date | no | Query on a specific updated_at Example: `2000-01-01T12:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "avatarUrl": "https://example.com",
        "churchCenterEnabled": true,
        "city": "string",
        "contactEmailAddress": "ava@example.com",
        "country": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "dateFormat": 1,
        "description": "string",
        "geolocationSetManually": true,
        "latitude": 1,
        "longitude": 1,
        "name": "Ava Chen",
        "phoneNumber": "string",
        "state": "string",
        "street": "string",
        "timeZone": "string",
        "timeZoneRaw": "string",
        "twentyFourHourTime": true,
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "website": "string",
        "zip": "string"
      },
      "id": "string",
      "relationships": {
        "organization": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.avatarUrl` | string |  |
| `attributes.churchCenterEnabled` | boolean |  |
| `attributes.city` | string |  |
| `attributes.contactEmailAddress` | string |  |
| `attributes.country` | string |  |
| `attributes.createdAt` | date |  |
| `attributes.dateFormat` | number |  |
| `attributes.description` | string |  |
| `attributes.geolocationSetManually` | boolean |  |
| `attributes.latitude` | number |  |
| `attributes.longitude` | number |  |
| `attributes.name` | string |  |
| `attributes.phoneNumber` | string |  |
| `attributes.state` | string |  |
| `attributes.street` | string |  |
| `attributes.timeZone` | string |  |
| `attributes.timeZoneRaw` | string |  |
| `attributes.twentyFourHourTime` | boolean |  |
| `attributes.updatedAt` | date |  |
| `attributes.website` | string |  |
| `attributes.zip` | string |  |
| `id` | string |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Planning Center API, this operation is `GET /people/v2/campuses` (base URL `https://api.planningcenteronline.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campuses.md) for the provider-specific parameters and requirements.

