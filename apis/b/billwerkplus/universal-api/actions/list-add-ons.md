# Billwerkplus: List Add-Ons

Retrieves add-ons from Billwerkplus.

```
GET https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/list-add-ons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/list-add-ons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/list-add-ons?${params}`, {
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
| `range` | list | no | Time attribute to limit by: created or deleted. One of: `0`, `1`. Default: `created`. |
| `handle` | string | no | Exact add-on handle. |
| `handlePrefix` | string | no | Add-on handle prefix. |
| `state` | list | no | Add-on state: active or deleted. One of: `0`, `1`. Default: `active`. |
| `type` | list | no | Add-on type: on_off or quantity. One of: `0`, `1`. |
| `name` | string | no | Add-on name filter. |
| `plan` | string | no | Plan handle filter. |
| `currency[]` | array<string> | no | Currency filter. Multiple values are allowed. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | date | no | Inclusive start of the local account time range. |
| `to` | date | no | Exclusive end of the local account time range. |
| `interval` | string | no | ISO 8601 duration counted back from To. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        {
          "allPlans": true,
          "amount": 1,
          "amountInclVat": true,
          "created": "string",
          "currency": "string",
          "description": "string",
          "handle": "string",
          "name": "Ava Chen",
          "state": "string",
          "type": "string",
          "vat": 1
        }
      ],
      "count": 1,
      "from": "string",
      "range": "string",
      "size": 1,
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[].allPlans` | boolean |  |
| `content[].amount` | number |  |
| `content[].amountInclVat` | boolean |  |
| `content[].created` | string |  |
| `content[].currency` | string |  |
| `content[].description` | string |  |
| `content[].handle` | string |  |
| `content[].name` | string |  |
| `content[].state` | string |  |
| `content[].type` | string |  |
| `content[].vat` | number |  |
| `count` | number |  |
| `from` | string |  |
| `range` | string |  |
| `size` | number |  |
| `to` | string |  |

## Native endpoint

Through the native Billwerkplus API, this operation is `GET /list/add_on` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-add-ons.md) for the provider-specific parameters and requirements.

