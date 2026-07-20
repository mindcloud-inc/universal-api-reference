# Retently: Add Suppressed Domain

Creates a suppressed domain entry in Retently.

```
POST https://connect.mindcloud.co/v1/universal/retently/latest/actions/add-suppressed-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/retently/latest/actions/add-suppressed-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pattern": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retently/latest/actions/add-suppressed-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pattern": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pattern` | string | yes | The domain pattern to suppress. Supports wildcards (e.g., *.example.com); |
| `category` | string | no | Category of the domain. Values: other (default), corporate, disposable, invalid; Default: `other`. |
| `note` | string | no | An optional note explaining why the domain was suppressed; |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedBy": "string",
      "category": "string",
      "createdAt": "string",
      "id": "string",
      "note": "string",
      "pattern": "string",
      "reason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedBy` | string |  |
| `category` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `note` | string |  |
| `pattern` | string |  |
| `reason` | string |  |

## Native endpoint

Through the native Retently API, this operation is `POST /api/v2/suppressions/domains` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-suppressed-domain.md) for the provider-specific parameters and requirements.

