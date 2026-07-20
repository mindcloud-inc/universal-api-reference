# Quickbase: Insert/Update Record(s)

Creates Quickbase records, or updates matching records if they exist.

```
POST https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/insert-update-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quickbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/insert-update-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string",
  "data": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/insert-update-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string",
    "data": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes | The Quickbase table identifier that will receive the record changes. |
| `data` | string<string> | yes | JSON string containing the Quickbase record array payload, for example [{"6":{"value":"Acme"}}]. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Returned record data when Quickbase includes it. |
| `metadata` | object | Information about created, updated, unchanged, or failed records. |

## Native endpoint

Through the native Quickbase API, this operation is `POST v1/records` (base URL `https://api.quickbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-update-records.md) for the provider-specific parameters and requirements.

