# Centerpoint: Get Service Agreement



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-service-agreement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-service-agreement?connectionId=$CONNECTION_ID&SERVICE_AGREEMENT_ID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "SERVICE_AGREEMENT_ID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-service-agreement?${params}`, {
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
| `SERVICE_AGREEMENT_ID` | number | yes |  |

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
        "custom": {
          "reachoutdate": {},
          "type": {}
        },
        "deletedAt": {},
        "frequency": "string",
        "name": "Ava Chen",
        "nextInspectionDate": "string",
        "note": {},
        "price": "string",
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
        "file": {
          "data": {}
        },
        "profile": {
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
| `attributes.custom.reachoutdate` | object |  |
| `attributes.custom.type` | object |  |
| `attributes.deletedAt` | object |  |
| `attributes.frequency` | string |  |
| `attributes.name` | string |  |
| `attributes.nextInspectionDate` | string |  |
| `attributes.note` | object |  |
| `attributes.price` | string |  |
| `attributes.startDate` | string |  |
| `attributes.terminatedAt` | object |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `relationships.company.data.id` | string |  |
| `relationships.company.data.type` | string |  |
| `relationships.createdBy.data.id` | string |  |
| `relationships.createdBy.data.type` | string |  |
| `relationships.file.data` | object |  |
| `relationships.profile.data.id` | string |  |
| `relationships.profile.data.type` | string |  |
| `relationships.property.data.id` | string |  |
| `relationships.property.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET service_agreements/:SERVICE_AGREEMENT_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-agreement.md) for the provider-specific parameters and requirements.

