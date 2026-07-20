# Swell: Create Variant



```
POST https://connect.mindcloud.co/v1/universal/swell/latest/actions/create-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swell/latest/actions/create-variant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swell/latest/actions/create-variant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parentId` | string | yes | The parent product ID. |
| `name` | string | no | The variant name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "parentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `currency` | string |  |
| `dateCreated` | date |  |
| `id` | string |  |
| `name` | string |  |
| `parentId` | string |  |

## Native endpoint

Through the native Swell API, this operation is `POST /products\:variants` (base URL `https://api.swell.store`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-variant.md) for the provider-specific parameters and requirements.

