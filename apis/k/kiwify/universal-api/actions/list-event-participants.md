# Kiwify: List Event Participants

Retrieves event participants from Kiwify.

```
GET https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/list-event-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/list-event-participants?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/list-event-participants?${params}`, {
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
| `productId` | string | yes |  |
| `checkedIn` | boolean | no |  |
| `pageSize` | string | no |  |
| `pageNumber` | string | no |  |
| `createdAtStartDate` | string | no |  |
| `createdAtEndDate` | string | no |  |
| `updatedAtStartDate` | string | no |  |
| `updatedAtEndDate` | string | no |  |
| `externalId` | string | no |  |
| `batchId` | string | no |  |
| `phone` | string | no |  |
| `cpf` | string | no |  |
| `orderId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<string> |  |
| `pagination` | object |  |

## Native endpoint

Through the native Kiwify API, this operation is `GET /v1/events/:product_id/participants` (base URL `https://public-api.kiwify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-participants.md) for the provider-specific parameters and requirements.

