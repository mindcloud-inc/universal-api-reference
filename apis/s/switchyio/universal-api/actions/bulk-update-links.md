# Switchy.io: Bulk Update Links

Updates existing links in Switchy.io by domain and IDs.

```
PUT https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/bulk-update-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Switchy.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/bulk-update-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string",
  "idsCsv": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/bulk-update-links', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string",
    "idsCsv": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes |  |
| `idsCsv` | string | yes | Comma-separated link ids within the selected domain |
| `url` | string | no |  |
| `title` | string | no |  |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affected_rows": 1,
      "returning": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affected_rows` | number |  |
| `returning` | array<object> |  |

## Native endpoint

Through the native Switchy.io API, this operation is `POST /v1/graphql` (base URL `https://graphql.switchy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-links.md) for the provider-specific parameters and requirements.

