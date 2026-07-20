# Rulebricks: Import Rule

Creates or updates a rule in Rulebricks.

```
POST https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/import-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rulebricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/import-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rule": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/import-rule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rule": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rule` | object | yes | Rule object accepted by the Rulebricks import endpoint |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Rule ID |
| `name` | string | Rule name |
| `slug` | string | Rule slug |

## Native endpoint

Through the native Rulebricks API, this operation is `POST /admin/rules/import` (base URL `https://rulebricks.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-rule.md) for the provider-specific parameters and requirements.

