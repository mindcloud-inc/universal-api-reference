# Mendato: Get Object



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-object?connectionId=$CONNECTION_ID&variables=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-object?${params}`, {
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
| `variables` | object | yes | GraphQL variables object for the Mendato object query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "object": {
        "addressSupplement": "string",
        "city": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "number": 1,
        "phone": "string",
        "streetAddress": "string",
        "zip": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `object.addressSupplement` | string |  |
| `object.city` | string |  |
| `object.createdAt` | date |  |
| `object.email` | string |  |
| `object.id` | string |  |
| `object.name` | string |  |
| `object.number` | number |  |
| `object.phone` | string |  |
| `object.streetAddress` | string |  |
| `object.zip` | string |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-object.md) for the provider-specific parameters and requirements.

