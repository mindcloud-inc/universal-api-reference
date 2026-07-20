# BlockSurvey: Get Contact

Retrieves a contact from BlockSurvey.

```
GET https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlockSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/get-contact?connectionId=$CONNECTION_ID&teamId=string&listId=string&listPrivateKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "listId": "string",
  "listPrivateKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/get-contact?${params}`, {
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
| `teamId` | string | yes | ID of the team owning the list. |
| `listId` | string | yes | ID of the list containing the contact. |
| `listPrivateKey` | string | yes | Private key for decryption. |
| `recordId` | string | no | ID of the contact to retrieve. |
| `email` | string | no | Email of the contact to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactDetails": {
        "Country": "string",
        "Email": "ava@example.com",
        "First Name": "Ava Chen",
        "Last Name": "Ava Chen",
        "Phone Number": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactDetails` | object |  |
| `contactDetails.Country` | string |  |
| `contactDetails.Email` | string |  |
| `contactDetails.First Name` | string |  |
| `contactDetails.Last Name` | string |  |
| `contactDetails.Phone Number` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native BlockSurvey API, this operation is `POST /contact/get-contact` (base URL `https://api3.blocksurvey.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

