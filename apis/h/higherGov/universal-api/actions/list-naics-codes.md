# HigherGov: List NAICS Codes

Retrieves NAICS codes from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-naics-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-naics-codes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-naics-codes?${params}`, {
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
| `naicsCode` | string | no | Awards NAICS code |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "naics_code": "string",
      "naics_description": "string",
      "naics_description_long": "string",
      "path": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `naics_code` | string |  |
| `naics_description` | string |  |
| `naics_description_long` | string |  |
| `path` | string |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/naics/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-naics-codes.md) for the provider-specific parameters and requirements.

