# Simplicate: Update Person



```
PUT https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/update-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/update-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/update-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | The person's email address |
| `familyName` | string | no | The person's family name |
| `firstName` | string | no | The person's first name |
| `id` | string | yes | The person's id |
| `note` | string | no | A note for the person |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `PUT /crm/person/:id` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person.md) for the provider-specific parameters and requirements.

