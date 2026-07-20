# Follow Up Boss - Legacy: List Events

Retrieves events from Follow Up Boss - Legacy.

```
GET https://connect.mindcloud.co/v1/universal/followUpBoss/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss - Legacy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBoss/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBoss/latest/actions/list-events?${params}`, {
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
| `createDate` | string | no |  |
| `hasProperty` | boolean | no |  |
| `next` | string | no |  |
| `personId` | int32 | no |  |
| `propertyAddress` | string | no |  |
| `type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "message": "string",
      "occurred": "2026-05-07T12:00:00.000Z",
      "pageDuration": 1,
      "pageUrl": "https://example.com",
      "personId": 1,
      "property": {
        "city": "string",
        "code": "string",
        "forRent": 1,
        "id": 1,
        "lat": 1,
        "lng": 1,
        "lot": "string",
        "mlsNumber": "string",
        "price": "string",
        "state": "string",
        "street": "string",
        "type": "string",
        "url": "https://example.com"
      },
      "source": "string",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `description` | string |  |
| `id` | number |  |
| `message` | string |  |
| `occurred` | date |  |
| `pageDuration` | number |  |
| `pageUrl` | string |  |
| `personId` | number |  |
| `property.city` | string |  |
| `property.code` | string |  |
| `property.forRent` | number |  |
| `property.id` | number |  |
| `property.lat` | number |  |
| `property.lng` | number |  |
| `property.lot` | string |  |
| `property.mlsNumber` | string |  |
| `property.price` | string |  |
| `property.state` | string |  |
| `property.street` | string |  |
| `property.type` | string |  |
| `property.url` | string |  |
| `source` | string |  |
| `type` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Follow Up Boss - Legacy API, this operation is `GET events` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

