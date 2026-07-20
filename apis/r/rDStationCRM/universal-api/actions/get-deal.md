# RD Station CRM: Get Deal

Retrieves deal details from RD Station CRM.

```
GET https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/get-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/get-deal?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/get-deal?${params}`, {
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
| `id` | string | yes | Deal identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contactIds": [
          [
            "string"
          ]
        ],
        "createdAt": "string",
        "customFields": {},
        "id": "string",
        "name": "Ava Chen",
        "oneTimePrice": 1,
        "ownerId": "string",
        "pipelineId": "string",
        "rating": 1,
        "recurrencePrice": 1,
        "stageId": "string",
        "status": "string",
        "totalPrice": 1,
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
| `data.contactIds[]` | array<string> |  |
| `data.createdAt` | string |  |
| `data.customFields` | object |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.oneTimePrice` | number |  |
| `data.ownerId` | string |  |
| `data.pipelineId` | string |  |
| `data.rating` | number |  |
| `data.recurrencePrice` | number |  |
| `data.stageId` | string |  |
| `data.status` | string |  |
| `data.totalPrice` | number |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native RD Station CRM API, this operation is `GET /deals/:id` (base URL `https://api.rd.services/crm/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal.md) for the provider-specific parameters and requirements.

