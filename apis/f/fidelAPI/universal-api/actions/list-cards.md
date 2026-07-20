# Fidel API: List Cards

Retrieves cards from a Fidel program.

```
GET https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-cards?connectionId=$CONNECTION_ID&limit=25&offset=0&programId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "programId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-cards?${params}`, {
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
      "countryCode": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "expDate": "2026-05-07T12:00:00.000Z",
      "expMonth": 1,
      "expYear": 1,
      "firstNumbers": "string",
      "id": "string",
      "lastNumbers": "string",
      "live": true,
      "programId": "string",
      "scheme": "string",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `countryCode` | string |  |
| `created` | date |  |
| `expDate` | date |  |
| `expMonth` | number |  |
| `expYear` | number |  |
| `firstNumbers` | string |  |
| `id` | string |  |
| `lastNumbers` | string |  |
| `live` | boolean |  |
| `programId` | string |  |
| `scheme` | string |  |
| `type` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Fidel API API, this operation is `GET /programs/:programId/cards` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-cards.md) for the provider-specific parameters and requirements.

