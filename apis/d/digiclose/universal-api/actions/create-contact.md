# Digiclose: Create Contact



```
POST https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digiclose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fields": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | object | yes | Contact field values using Digiclose internal field names. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {
          "id": 1,
          "name": "Ava Chen",
          "value": "string"
        }
      ],
      "id": 1,
      "links": {
        "contact": {
          "href": "https://example.com",
          "type": "https://example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields[].id` | number |  |
| `fields[].name` | string |  |
| `fields[].value` | string |  |
| `id` | number |  |
| `links.contact.href` | string |  |
| `links.contact.type` | string |  |

## Native endpoint

Through the native Digiclose API, this operation is `POST /contacts` (base URL `https://app.digiclose.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

