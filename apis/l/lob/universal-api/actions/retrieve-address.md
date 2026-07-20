# Lob: Retrieve Address



```
GET https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-address?connectionId=$CONNECTION_ID&adr_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adr_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-address?${params}`, {
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
| `adr_id` | string | yes | The Lob address ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address_city": "string",
      "address_country": "string",
      "address_line1": "string",
      "address_line2": "string",
      "address_state": "string",
      "address_zip": "string",
      "company": "string",
      "date_created": "string",
      "date_modified": "string",
      "description": "string",
      "email": "ava@example.com",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "object": "string",
      "phone": "string",
      "recipient_moved": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_city` | string |  |
| `address_country` | string |  |
| `address_line1` | string |  |
| `address_line2` | string |  |
| `address_state` | string |  |
| `address_zip` | string |  |
| `company` | string |  |
| `date_created` | string |  |
| `date_modified` | string |  |
| `description` | string |  |
| `email` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `object` | string |  |
| `phone` | string |  |
| `recipient_moved` | boolean |  |

## Native endpoint

Through the native Lob API, this operation is `GET /addresses/:adr_id` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-address.md) for the provider-specific parameters and requirements.

