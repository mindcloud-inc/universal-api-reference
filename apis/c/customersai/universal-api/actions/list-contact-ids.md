# Customers.ai: List Contact IDs



```
GET https://connect.mindcloud.co/v1/universal/customersai/latest/actions/list-contact-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customers.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customersai/latest/actions/list-contact-ids?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customersai/latest/actions/list-contact-ids?${params}`, {
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
| `email` | string | no | Filter contacts by email address. |
| `firstName` | string | no | Filter contacts by first name. |
| `lastName` | string | no | Filter contacts by last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ids": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ids` | array<number> | Matching contact IDs returned by Customers.ai. |

## Native endpoint

Through the native Customers.ai API, this operation is `GET /contacts/ids` (base URL `https://api.mobilemonkey.com/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-ids.md) for the provider-specific parameters and requirements.

