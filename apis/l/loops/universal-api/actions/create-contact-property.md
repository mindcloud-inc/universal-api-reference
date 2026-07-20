# Loops: Create Contact Property

Creates a new contact property in Loops.

```
POST https://connect.mindcloud.co/v1/universal/loops/latest/actions/create-contact-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loops `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loops/latest/actions/create-contact-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "boolean"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loops/latest/actions/create-contact-property', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "boolean"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `type` | list | yes | One of: `boolean`, `date`, `number`, `string`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Loops API, this operation is `POST /contacts/properties` (base URL `https://app.loops.so/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-property.md) for the provider-specific parameters and requirements.

