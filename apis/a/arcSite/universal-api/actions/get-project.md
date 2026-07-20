# ArcSite: Get Project

Retrieves one project by ID from ArcSite.

```
GET https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ArcSite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/get-project?${params}`, {
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
| `projectId` | string | yes | The ID of the project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customer": {
        "address": {
          "city": {},
          "county": {},
          "state": {},
          "street": {},
          "zipCode": {}
        },
        "email": {},
        "name": {},
        "phone": {},
        "secondEmail": {},
        "secondPhone": {}
      },
      "id": "string",
      "jobNumber": "string",
      "name": "Ava Chen",
      "salesRep": {
        "email": {},
        "name": {},
        "phone": {}
      },
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workSiteAddress": {}
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
| `customer.address.city` | object |  |
| `customer.address.county` | object |  |
| `customer.address.state` | object |  |
| `customer.address.street` | object |  |
| `customer.address.zipCode` | object |  |
| `customer.email` | object |  |
| `customer.name` | object |  |
| `customer.phone` | object |  |
| `customer.secondEmail` | object |  |
| `customer.secondPhone` | object |  |
| `id` | string |  |
| `jobNumber` | string |  |
| `name` | string |  |
| `salesRep.email` | object |  |
| `salesRep.name` | object |  |
| `salesRep.phone` | object |  |
| `updatedAt` | date |  |
| `workSiteAddress` | object |  |

## Native endpoint

Through the native ArcSite API, this operation is `GET /projects/:projectId` (base URL `https://api.arcsite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

