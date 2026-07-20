# BlockSurvey: Update Contact

Updates an existing contact in BlockSurvey.

```
PUT https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlockSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "listId": "string",
  "listPublicKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "listId": "string",
    "listPublicKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | ID of the team owning the list. |
| `listId` | string | yes | ID of the list containing the contact. |
| `listPublicKey` | string | yes | Public key for encryption. |
| `recordId` | string | no | ID of the contact to update. |
| `oldEmail` | string | no | Old email of the contact. |
| `email` | string | no | New email of the contact. |
| `firstName` | string | no | First name of the contact. |
| `lastName` | string | no | Last name of the contact. |
| `phoneNumber` | string | no | Phone number of the contact. |
| `country` | string | no | Country of the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recordId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recordId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native BlockSurvey API, this operation is `PUT /contact/update-contact` (base URL `https://api3.blocksurvey.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

