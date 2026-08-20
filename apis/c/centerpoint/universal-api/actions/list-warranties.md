# Centerpoint: List Warranties



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-warranties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-warranties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-warranties?${params}`, {
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
| `fields[companies]` | string | no |  |
| `fields[properties]` | string | no |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": "string",
        "deletedAt": {},
        "endDate": "string",
        "manufacturer": {},
        "name": "Ava Chen",
        "startDate": "string",
        "status": "string",
        "updatedAt": "string",
        "years": 1
      },
      "id": "string",
      "relationships": {
        "company": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "contractorCompany": {
          "data": {}
        },
        "file": {
          "data": {
            "id": "string",
            "type": "string"
          }
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
| `attributes.deletedAt` | object |  |
| `attributes.endDate` | string |  |
| `attributes.manufacturer` | object |  |
| `attributes.name` | string |  |
| `attributes.startDate` | string |  |
| `attributes.status` | string |  |
| `attributes.updatedAt` | string |  |
| `attributes.years` | number |  |
| `id` | string |  |
| `relationships.company.data.id` | string |  |
| `relationships.company.data.type` | string |  |
| `relationships.contractorCompany.data` | object |  |
| `relationships.file.data.id` | string |  |
| `relationships.file.data.type` | string |  |
| `relationships.property.data.id` | string |  |
| `relationships.property.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET warranties` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-warranties.md) for the provider-specific parameters and requirements.

