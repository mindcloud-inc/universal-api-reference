# Centerpoint: List Service Agreements



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-service-agreements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-service-agreements?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-service-agreements?${params}`, {
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
| `fields[properties]` | string | no |  |
| `fields[buildings]` | string | no |  |
| `fields[companies]` | string | no |  |
| `fields[profiles]` | string | no |  |
| `fields[employees]` | string | no |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": "string",
        "custom": {
          "reachoutdate": "string",
          "type": "string"
        },
        "deletedAt": {},
        "frequency": "string",
        "name": "Ava Chen",
        "nextInspectionDate": "string",
        "note": {},
        "price": {},
        "startDate": "string",
        "terminatedAt": {},
        "updatedAt": "string"
      },
      "id": "string",
      "relationships": {
        "company": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "createdBy": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "profile": {
          "data": {}
        },
        "property": {
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
| `attributes.createdAt` | string |  |
| `attributes.custom.reachoutdate` | string |  |
| `attributes.custom.type` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.frequency` | string |  |
| `attributes.name` | string |  |
| `attributes.nextInspectionDate` | string |  |
| `attributes.note` | object |  |
| `attributes.price` | object |  |
| `attributes.startDate` | string |  |
| `attributes.terminatedAt` | object |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `relationships.company.data.id` | string |  |
| `relationships.company.data.type` | string |  |
| `relationships.createdBy.data.id` | string |  |
| `relationships.createdBy.data.type` | string |  |
| `relationships.profile.data` | object |  |
| `relationships.property.data.id` | string |  |
| `relationships.property.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET service_agreements` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-service-agreements.md) for the provider-specific parameters and requirements.

