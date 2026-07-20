# Marketing Master IO: Create Contact Tag

Creates a new contact tag in Marketing Master IO.

```
POST https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/create-contact-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/create-contact-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "page_data_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/create-contact-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "page_data_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Contact tag name. |
| `page_data_id` | string | yes | Page data ID associated with the tag. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `status` | boolean |  |

## Native endpoint

Through the native Marketing Master IO API, this operation is `POST /v1/contacts/tags` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-tag.md) for the provider-specific parameters and requirements.

