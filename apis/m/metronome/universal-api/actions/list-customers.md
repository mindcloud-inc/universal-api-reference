# Metronome: List Customers

Retrieves customers from Metronome.

```
GET https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-customers?${params}`, {
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
| `ingestAlias` | string | no | Filter the customer list by ingest alias. |
| `customerIds[]` | array<string> | no | Filter the customer list by customer ID. Accepts multiple values as an array. |
| `onlyArchived` | boolean | no | Only return archived customers. |
| `salesforceAccountIds[]` | array<string> | no | Filter the customer list by Salesforce account ID. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "external_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `external_id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Metronome API, this operation is `GET /v1/customers` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

