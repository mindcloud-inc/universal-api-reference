# Centerpoint: Get cost_code



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-cost-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-cost-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-cost-code?${params}`, {
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
| `include` | string | no | Example: `budget`. |
| `COST_CODE_ID` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": "string",
        "deletedAt": {},
        "name": "Ava Chen",
        "spent": 1,
        "type": "string",
        "updatedAt": "string",
        "value": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.name` | string |  |
| `attributes.spent` | number |  |
| `attributes.type` | string |  |
| `attributes.updatedAt` | string |  |
| `attributes.value` | number |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET cost_codes` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cost-code.md) for the provider-specific parameters and requirements.

