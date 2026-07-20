# HigherGov: List Agencies

Retrieves agencies from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-agencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-agencies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-agencies?${params}`, {
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
| `agencyKey` | string | no | HigherGov Agency key |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agency_abbreviation": "string",
      "agency_key": 1,
      "agency_name": "Ava Chen",
      "agency_type": "string",
      "defense_flag": true,
      "path": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agency_abbreviation` | string | Agency abbreviation |
| `agency_key` | number | HigherGov Agency key |
| `agency_name` | string | Agency name |
| `agency_type` | string | Agency type |
| `defense_flag` | boolean | Whether the agency is defense-related |
| `path` | string | HigherGov path |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/agency/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-agencies.md) for the provider-specific parameters and requirements.

