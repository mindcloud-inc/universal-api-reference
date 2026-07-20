# Returnless: List Customer Groups

Retrieves customer groups from Returnless.

```
GET https://connect.mindcloud.co/v1/universal/returnless/latest/actions/list-customer-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Returnless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/returnless/latest/actions/list-customer-groups?connectionId=$CONNECTION_ID&customer=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customer": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/returnless/latest/actions/list-customer-groups?${params}`, {
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
| `customer` | string | yes | The unique identifier of the customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "links": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Collection payload for this Returnless list endpoint. |
| `links` | object | Pagination links. |
| `meta` | object | Pagination metadata. |

## Native endpoint

Through the native Returnless API, this operation is `GET /2025-01/customers/{customer}/customer-groups` (base URL `https://api-v2.returnless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-groups.md) for the provider-specific parameters and requirements.

