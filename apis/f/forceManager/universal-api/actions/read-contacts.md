# ForceManager: Read Contacts

Retrieves contacts from your ForceManager account.

```
GET https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native ForceManager API, this operation is `GET /contacts`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-contacts.md) for the provider-specific parameters and requirements.

