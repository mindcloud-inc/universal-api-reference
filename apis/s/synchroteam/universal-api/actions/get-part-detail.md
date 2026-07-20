# Synchroteam: Get Part Detail

Retrieves a part from Synchroteam by supported identifier.

```
GET https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-part-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-part-detail?connectionId=$CONNECTION_ID&identifierType=string&identifierValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifierType": "string",
  "identifierValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-part-detail?${params}`, {
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
| `identifierType` | string | yes | Which identifier to use (for example: reference, id). |
| `identifierValue` | string | yes | The identifier value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "minQuantity": 1,
      "name": "Ava Chen",
      "price": 1,
      "reference": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `minQuantity` | number |  |
| `name` | string |  |
| `price` | number |  |
| `reference` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `GET /Api/v2/Part/Details` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-part-detail.md) for the provider-specific parameters and requirements.

