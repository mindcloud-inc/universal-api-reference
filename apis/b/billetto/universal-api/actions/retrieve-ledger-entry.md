# Billetto: Retrieve Ledger Entry

Retrieves a ledger entry from Billetto.

```
GET https://connect.mindcloud.co/v1/universal/billetto/latest/actions/retrieve-ledger-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billetto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billetto/latest/actions/retrieve-ledger-entry?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billetto/latest/actions/retrieve-ledger-entry?${params}`, {
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
| `id` | string | yes | Billetto ledger entry ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entry_type": "string",
      "id": "string",
      "kind": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entry_type` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `object` | string |  |

## Native endpoint

Through the native Billetto API, this operation is `GET organiser/ledger_entries/{id}` (base URL `https://billetto.dk/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-ledger-entry.md) for the provider-specific parameters and requirements.

