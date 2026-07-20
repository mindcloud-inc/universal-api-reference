# Copperx: Get Tax Rate

Retrieves a tax rate from Copperx.

```
GET https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-tax-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-tax-rate?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-tax-rate?${params}`, {
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
| `id` | string | yes | Tax rate ID path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "isActive": true,
      "metadata": {},
      "name": "Ava Chen",
      "percentage": 1,
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `metadata` | object |  |
| `name` | string |  |
| `percentage` | number |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Copperx API, this operation is `GET /tax-rates/{id}` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tax-rate.md) for the provider-specific parameters and requirements.

