# Planning Center: List Person Addresses

Retrieves addresses for a person in Planning Center.

```
GET https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-person-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planning Center `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-person-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-person-addresses?${params}`, {
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
| `personId` | string | yes |  |
| `where.city` | string | no |  |
| `where.countryCode` | string | no |  |
| `where.location` | string | no |  |
| `where.primary` | boolean | no |  |
| `where.state` | string | no |  |
| `where.streetLine1` | string | no |  |
| `where.streetLine2` | string | no |  |
| `where.zip` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "city": "string",
        "countryCode": "string",
        "countryName": "Ava Chen",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "location": "string",
        "primary": true,
        "state": "string",
        "streetLine1": "string",
        "streetLine2": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "zip": "string"
      },
      "id": "string",
      "relationships": {
        "person": {
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
| `attributes.city` | string |  |
| `attributes.countryCode` | string |  |
| `attributes.countryName` | string |  |
| `attributes.createdAt` | date |  |
| `attributes.location` | string |  |
| `attributes.primary` | boolean |  |
| `attributes.state` | string |  |
| `attributes.streetLine1` | string |  |
| `attributes.streetLine2` | string |  |
| `attributes.updatedAt` | date |  |
| `attributes.zip` | string |  |
| `id` | string |  |
| `relationships.person.data.id` | string |  |
| `relationships.person.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Planning Center API, this operation is `GET /people/v2/people/:person_id/addresses` (base URL `https://api.planningcenteronline.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-person-addresses.md) for the provider-specific parameters and requirements.

