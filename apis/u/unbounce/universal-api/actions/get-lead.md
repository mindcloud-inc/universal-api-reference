# Unbounce: Get Lead

Retrieves a specific lead from Unbounce.

```
GET https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unbounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/get-lead?connectionId=$CONNECTION_ID&lead_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lead_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/get-lead?${params}`, {
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
| `lead_id` | string | yes | Unbounce lead ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "extraData": {},
      "formData": {},
      "id": "string",
      "metadata": {},
      "pageId": "string",
      "submitterIp": "string",
      "variantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `extraData` | object |  |
| `formData` | object |  |
| `id` | string |  |
| `metadata` | object |  |
| `pageId` | string |  |
| `submitterIp` | string |  |
| `variantId` | string |  |

## Native endpoint

Through the native Unbounce API, this operation is `GET /leads/:lead_id` (base URL `https://api.unbounce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

