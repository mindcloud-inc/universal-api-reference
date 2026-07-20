# Voucherify: Get Publication



```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-publication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-publication?connectionId=$CONNECTION_ID&publicationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-publication?${params}`, {
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
| `publicationId` | string | yes | Voucherify publication identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignName": "Ava Chen",
      "customerId": "string",
      "id": "string",
      "object": "string",
      "result": "string",
      "voucherCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignName` | string |  |
| `customerId` | string |  |
| `id` | string |  |
| `object` | string |  |
| `result` | string |  |
| `voucherCode` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `GET /publications/:publicationId` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-publication.md) for the provider-specific parameters and requirements.

