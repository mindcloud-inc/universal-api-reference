# BunnyCDN: Get Billing Summary Document

Retrieves a BunnyCDN billing summary PDF.

```
GET https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-billing-summary-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-billing-summary-document?connectionId=$CONNECTION_ID&billingRecordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "billingRecordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-billing-summary-document?${params}`, {
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
| `billingRecordId` | string | yes | The Bunny billing summary record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Raw PDF response body or empty body from Bunny billing summary document endpoint. |

## Native endpoint

Through the native BunnyCDN API, this operation is `GET /billing/summary/:billingRecordId/pdf` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-billing-summary-document.md) for the provider-specific parameters and requirements.

