# Kladana: Get Counterparty

Retrieves a counterparty record from Kladana.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-counterparty
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-counterparty?connectionId=$CONNECTION_ID&id=7944ef04-f831-11e5-7a69-971500188b19" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "7944ef04-f831-11e5-7a69-971500188b19"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-counterparty?${params}`, {
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
| `id` | string | yes | Kladana counterparty ID from the Counterparty resource URL. Example: `7944ef04-f831-11e5-7a69-971500188b19`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {}
      ],
      "actualAddress": "string",
      "archived": true,
      "code": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalCode": "string",
      "group": {},
      "id": "string",
      "inn": "string",
      "kpp": "string",
      "legalTitle": "string",
      "meta": {},
      "name": "Ava Chen",
      "ogrn": "string",
      "owner": {},
      "phone": "string",
      "shared": true,
      "tags": [
        "string"
      ],
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> | Bank accounts. |
| `actualAddress` | string | Actual address. |
| `archived` | boolean | Whether the counterparty is archived. |
| `code` | string | Internal code. |
| `created` | date | Creation timestamp. |
| `email` | string | Email address. |
| `externalCode` | string | External code. |
| `group` | object | Group reference. |
| `id` | string | Counterparty UUID. |
| `inn` | string | Taxpayer identifier. |
| `kpp` | string | Tax registration reason code. |
| `legalTitle` | string | Legal title. |
| `meta` | object | Kladana metadata reference. |
| `name` | string | Counterparty name. |
| `ogrn` | string | Registration number. |
| `owner` | object | Owner reference. |
| `phone` | string | Phone number. |
| `shared` | boolean | Whether the counterparty is shared. |
| `tags` | array<string> | Counterparty tags. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/counterparty/{id}` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-counterparty.md) for the provider-specific parameters and requirements.

