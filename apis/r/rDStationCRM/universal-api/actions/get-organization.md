# RD Station CRM: Get Organization

Retrieves organization details from RD Station CRM.

```
GET https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/get-organization?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/get-organization?${params}`, {
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
| `id` | string | yes | Organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "address": {},
        "createdAt": "string",
        "customFields": {},
        "description": "string",
        "followerIds": [
          [
            "string"
          ]
        ],
        "id": "string",
        "name": "Ava Chen",
        "ownerId": "string",
        "segmentIds": [
          [
            "string"
          ]
        ],
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.address` | object |  |
| `data.createdAt` | string |  |
| `data.customFields` | object |  |
| `data.description` | string |  |
| `data.followerIds[]` | array<string> |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.ownerId` | string |  |
| `data.segmentIds[]` | array<string> |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native RD Station CRM API, this operation is `GET /organizations/:id` (base URL `https://api.rd.services/crm/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

