# Paymo: List Clients

Retrieves clients from Paymo.

```
GET https://connect.mindcloud.co/v1/universal/paymo/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paymo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paymo/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paymo/latest/actions/list-clients?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `where` | string | no | Optional Paymo filtering expression, for example `name like Sample` or `id>0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "address": "string",
      "city": "string",
      "country": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "dueInterval": 1,
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "postalCode": "string",
      "state": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `address` | string |  |
| `city` | string |  |
| `country` | string |  |
| `createdOn` | date |  |
| `dueInterval` | number |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `postalCode` | string |  |
| `state` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Paymo API, this operation is `GET clients` (base URL `https://app.paymoapp.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

