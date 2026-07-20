# Deepgram: List Project Purchases

Retrieves project purchases from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-purchases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-purchases?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-purchases?${params}`, {
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
| `projectId` | string | yes | Deepgram project identifier. |
| `limit` | number | no | Number of purchases to return per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "created": "string",
      "orderId": "string",
      "orderType": "string",
      "units": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `created` | string |  |
| `orderId` | string |  |
| `orderType` | string |  |
| `units` | string |  |

## Native endpoint

Through the native Deepgram API, this operation is `GET /v1/projects/:project_id/purchases` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-purchases.md) for the provider-specific parameters and requirements.

