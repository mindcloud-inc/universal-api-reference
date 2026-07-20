# Constant Contact: Get Contact

Retrieves a contact from Constant Contact.

```
GET https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | yes | Unique ID of the contact to retrieve. |
| `include` | string | no | Include contact sub-resources in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createSource": "string",
      "emailAddress": {
        "address": "ava@example.com",
        "confirmStatus": "ava@example.com",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "optInDate": "2026-05-07T12:00:00.000Z",
        "optInSource": "ava@example.com",
        "permissionToSend": "ava@example.com",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "firstName": "Ava",
      "lastName": "Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |
| `createdAt` | date |  |
| `createSource` | string |  |
| `emailAddress` | object |  |
| `emailAddress.address` | string |  |
| `emailAddress.confirmStatus` | string |  |
| `emailAddress.createdAt` | date |  |
| `emailAddress.optInDate` | date |  |
| `emailAddress.optInSource` | string |  |
| `emailAddress.permissionToSend` | string |  |
| `emailAddress.updatedAt` | date |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Constant Contact API, this operation is `GET /contacts/:contact_id` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

