# BlockSurvey: Delete Contact

Deletes a contact from BlockSurvey.

```
DELETE https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlockSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/delete-contact?connectionId=$CONNECTION_ID&teamId=string&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/delete-contact?${params}`, {
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
| `recordId` | string | no | ID of the contact to delete. |
| `email` | string | no | Email of the contact to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native BlockSurvey API, this operation is `DELETE /contact/delete-contact` (base URL `https://api3.blocksurvey.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

