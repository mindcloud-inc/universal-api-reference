# GetResponse: Update Contact

Updates an existing contact in GetResponse.

```
PUT https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Unique identifier of the contact |
| `email` | string | no | Contact email address |
| `campaignId` | string | no | Campaign ID for the contact |
| `name` | string | no | Contact name |
| `dayOfCycle` | string | no | Autoresponder cycle day |
| `note` | string | no | Internal note for the contact |
| `scoring` | number | no | Contact scoring value |

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

Through the native GetResponse API, this operation is `POST /contacts/:contactId` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

