# ServiceTrade: Get Service Request by ID

Retrieves a service request from ServiceTrade by ID.

```
GET https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-service-request-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTrade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-service-request-by-id?connectionId=$CONNECTION_ID&serviceRequestId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serviceRequestId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-service-request-by-id?${params}`, {
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
| `serviceRequestId` | number | yes | ID of the service request to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asset": {
        "id": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "closedOn": 1,
      "contract": {
        "id": 1,
        "name": "Ava Chen"
      },
      "created": 1,
      "description": "string",
      "duration": 1,
      "estimatedPrice": 1,
      "id": 1,
      "items": [
        {
          "description": "string",
          "id": 1
        }
      ],
      "job": {
        "id": 1,
        "name": "Ava Chen",
        "number": 1,
        "type": "string"
      },
      "location": {
        "address": {
          "city": "string",
          "state": "string"
        },
        "id": 1,
        "name": "Ava Chen",
        "refNumber": "string",
        "status": "string"
      },
      "preferredStartTime": 1,
      "serviceLine": {
        "abbr": "string",
        "icon": "string",
        "id": 1,
        "name": "Ava Chen",
        "trade": "string"
      },
      "serviceLinkAttachmentVisibility": true,
      "serviceLinkCommentVisibility": true,
      "serviceRecurrence": {
        "description": "string",
        "frequency": "string",
        "id": 1,
        "interval": 1
      },
      "status": "string",
      "updated": 1,
      "uri": "string",
      "visibility": [
        "string"
      ],
      "windowEnd": 1,
      "windowStart": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asset.id` | number |  |
| `asset.name` | string |  |
| `asset.type` | string |  |
| `closedOn` | number |  |
| `contract.id` | number |  |
| `contract.name` | string |  |
| `created` | number |  |
| `description` | string |  |
| `duration` | number |  |
| `estimatedPrice` | number |  |
| `id` | number |  |
| `items[].description` | string |  |
| `items[].id` | number |  |
| `job.id` | number |  |
| `job.name` | string |  |
| `job.number` | number |  |
| `job.type` | string |  |
| `location.address.city` | string |  |
| `location.address.state` | string |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `location.refNumber` | string |  |
| `location.status` | string |  |
| `preferredStartTime` | number |  |
| `serviceLine.abbr` | string |  |
| `serviceLine.icon` | string |  |
| `serviceLine.id` | number |  |
| `serviceLine.name` | string |  |
| `serviceLine.trade` | string |  |
| `serviceLinkAttachmentVisibility` | boolean |  |
| `serviceLinkCommentVisibility` | boolean |  |
| `serviceRecurrence.description` | string |  |
| `serviceRecurrence.frequency` | string |  |
| `serviceRecurrence.id` | number |  |
| `serviceRecurrence.interval` | number |  |
| `status` | string |  |
| `updated` | number |  |
| `uri` | string |  |
| `visibility[]` | string |  |
| `windowEnd` | number |  |
| `windowStart` | number |  |

## Native endpoint

Through the native ServiceTrade API, this operation is `GET servicerequest/:serviceRequestId` (base URL `https://api.servicetrade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-request-by-id.md) for the provider-specific parameters and requirements.

