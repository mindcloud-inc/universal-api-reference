# ForceManager: Create Contact

Creates a new contact in ForceManager.

```
POST https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "gender": "string",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "gender": "string",
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `gender` | string | yes | Gender of the contact. |
| `firstName` | string | yes | First name of the contact. |
| `lastName` | string | yes | Last name of the contact. |
| `email` | string | yes | Email address of the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cityName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "gender": "string",
      "id": 1,
      "lastName": "Chen",
      "postcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cityName` | string | City name of the contact. |
| `email` | string | Email address of the contact. |
| `firstName` | string | First name of the contact. |
| `gender` | string | Gender of the contact. |
| `id` | number | Unique identifier for the contact. |
| `lastName` | string | Last name of the contact. |
| `postcode` | string | Postcode of the contact. |

## Native endpoint

Through the native ForceManager API, this operation is `POST /contacts`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

