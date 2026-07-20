# SimpleLocalize: Get Customer

Retrieves a customer from SimpleLocalize.

```
GET https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-customer?${params}`, {
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
| `customerKey` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "displayName": "Ava Chen",
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `displayName` | string |  |
| `key` | string |  |

## Native endpoint

Through the native SimpleLocalize API, this operation is `GET /api/v1/customers/{customerKey}` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

