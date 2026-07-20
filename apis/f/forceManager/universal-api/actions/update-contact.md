# ForceManager: Update Contact

Updates an existing contact in ForceManager.

```
PUT https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Unique identifier for the contact. |

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

Through the native ForceManager API, this operation is `PUT /contacts`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

