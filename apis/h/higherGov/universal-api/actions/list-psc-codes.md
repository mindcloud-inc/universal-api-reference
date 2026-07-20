# HigherGov: List PSC Codes

Retrieves PSC codes from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-psc-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-psc-codes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-psc-codes?${params}`, {
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
| `pscCode` | string | no | PSC code |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "path": "string",
      "psc_code": "string",
      "psc_description": "string",
      "psc_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `path` | string |  |
| `psc_code` | string |  |
| `psc_description` | string |  |
| `psc_name` | string |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/psc/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-psc-codes.md) for the provider-specific parameters and requirements.

