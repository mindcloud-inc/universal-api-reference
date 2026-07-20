# Mendato: Get Estimate



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-estimate?connectionId=$CONNECTION_ID&variables=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-estimate?${params}`, {
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
| `variables` | object | yes | GraphQL variables object for the Mendato estimate query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "estimate": {
        "acceptedAt": "2026-05-07T12:00:00.000Z",
        "completedAt": "2026-05-07T12:00:00.000Z",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "declinedAt": "2026-05-07T12:00:00.000Z",
        "declineReason": "string",
        "estimateDate": "2026-05-07T12:00:00.000Z",
        "hasKleinunternehmerregelung": true,
        "id": "string",
        "isAnsweredByCustomer": true,
        "number": 1,
        "numberPrefix": "string",
        "sentAt": "2026-05-07T12:00:00.000Z",
        "sentManually": true,
        "status": "string",
        "validityDate": "2026-05-07T12:00:00.000Z",
        "webEnabled": true,
        "webUrl": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `estimate.acceptedAt` | date |  |
| `estimate.completedAt` | date |  |
| `estimate.createdAt` | date |  |
| `estimate.declinedAt` | date |  |
| `estimate.declineReason` | string |  |
| `estimate.estimateDate` | date |  |
| `estimate.hasKleinunternehmerregelung` | boolean |  |
| `estimate.id` | string |  |
| `estimate.isAnsweredByCustomer` | boolean |  |
| `estimate.number` | number |  |
| `estimate.numberPrefix` | string |  |
| `estimate.sentAt` | date |  |
| `estimate.sentManually` | boolean |  |
| `estimate.status` | string |  |
| `estimate.validityDate` | date |  |
| `estimate.webEnabled` | boolean |  |
| `estimate.webUrl` | string |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-estimate.md) for the provider-specific parameters and requirements.

