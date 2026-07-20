# Alto: Get Contact Person

Retrieves a contact person from Alto by contact and person ID.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-contact-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-contact-person?connectionId=$CONNECTION_ID&contactId=string&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string",
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-contact-person?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Unique Alto contact identifier. |
| `personId` | string | yes | Unique Alto person identifier within the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailAddresses": [
        {}
      ],
      "forename": "Ava Chen",
      "id": "string",
      "isContactArchived": true,
      "phoneNumbers": [
        {}
      ],
      "surname": "Ava Chen",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAddresses` | array<object> |  |
| `forename` | string |  |
| `id` | string |  |
| `isContactArchived` | boolean |  |
| `phoneNumbers` | array<object> |  |
| `surname` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /contacts/:contactId/persons/:personId` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-person.md) for the provider-specific parameters and requirements.

