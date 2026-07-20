# Voucherify: Get Campaign

Retrieves a campaign from Voucherify.

```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | string | yes | Voucherify campaign identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignType": "string",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "object": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignType` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `object` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `GET /campaigns/:campaignId` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

