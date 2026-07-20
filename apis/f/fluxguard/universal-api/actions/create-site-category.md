# Fluxguard: Create Site Category

Creates a new site category in Fluxguard.

```
POST https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/create-site-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluxguard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/create-site-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/create-site-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for the new site category. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Creation timestamp of the site category. |
| `id` | string | Identifier of the created site category. |
| `name` | string | Name of the created site category. |

## Native endpoint

Through the native Fluxguard API, this operation is `POST /account/category` (base URL `https://api.fluxguard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site-category.md) for the provider-specific parameters and requirements.

