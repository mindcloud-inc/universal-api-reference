# MoreApp: Create Form

Creates a form in MoreApp.

```
POST https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "meta.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "meta.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes |  |
| `meta.name` | string | yes |  |
| `meta.description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "meta": {},
      "publishedVersion": {},
      "scope": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `meta` | object |  |
| `publishedVersion` | object |  |
| `scope` | string |  |
| `status` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `POST /api/v1.0/forms/customer/{{customerId}}/forms` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

