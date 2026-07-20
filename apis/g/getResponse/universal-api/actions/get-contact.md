# GetResponse: Get Contact

Retrieves contact details by ID from GetResponse.

```
GET https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | yes | Unique identifier of the contact |
| `fields` | string | no | Comma-separated list of fields to return |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {},
      "changedOn": "string",
      "contactId": "string",
      "createdOn": "string",
      "email": "ava@example.com",
      "href": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | object |  |
| `changedOn` | string |  |
| `contactId` | string |  |
| `createdOn` | string |  |
| `email` | string |  |
| `href` | string |  |
| `name` | string |  |

## Native endpoint

Through the native GetResponse API, this operation is `GET /contacts/:contactId` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

