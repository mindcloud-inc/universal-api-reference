# Centerpoint: Get Warranty



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-warranty
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-warranty?connectionId=$CONNECTION_ID&WARRANTY_ID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "WARRANTY_ID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-warranty?${params}`, {
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
| `WARRANTY_ID` | number | yes |  |

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
        "manufacturer": "string",
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
        "file": {
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
| `attributes.deletedAt` | object |  |
| `attributes.endDate` | string |  |
| `attributes.manufacturer` | string |  |
| `attributes.name` | string |  |
| `attributes.startDate` | string |  |
| `attributes.status` | string |  |
| `attributes.updatedAt` | string |  |
| `attributes.years` | number |  |
| `id` | string |  |
| `relationships.company.data.id` | string |  |
| `relationships.company.data.type` | string |  |
| `relationships.contractorCompany.data.id` | string |  |
| `relationships.contractorCompany.data.type` | string |  |
| `relationships.createdBy.data.id` | string |  |
| `relationships.createdBy.data.type` | string |  |
| `relationships.file.data` | object |  |
| `relationships.property.data.id` | string |  |
| `relationships.property.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET warranties/:WARRANTY_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-warranty.md) for the provider-specific parameters and requirements.

