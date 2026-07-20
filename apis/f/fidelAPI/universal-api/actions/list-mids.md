# Fidel API: List MIDs

Retrieves MIDs from a Fidel program.

```
GET https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-mids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-mids?connectionId=$CONNECTION_ID&limit=25&offset=0&programId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "programId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-mids?${params}`, {
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
| `programId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "brandId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isShared": true,
      "live": true,
      "locationId": "string",
      "mastercard": {},
      "programId": "string",
      "scheme": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "visa": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `brandId` | string |  |
| `created` | date |  |
| `id` | string |  |
| `isShared` | boolean |  |
| `live` | boolean |  |
| `locationId` | string |  |
| `mastercard` | object |  |
| `programId` | string |  |
| `scheme` | string |  |
| `updated` | date |  |
| `visa` | object |  |

## Native endpoint

Through the native Fidel API API, this operation is `GET /programs/:programId/mids` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-mids.md) for the provider-specific parameters and requirements.

