# Zoho FSM: Create Contact

Creates a new contact in Zoho FSM.

```
POST https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[0].Last_Name": "Chen",
  "data[0].Email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[0].Last_Name": "Chen",
    "data[0].Email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[]` | string | no |  |
| `data[0].Last_Name` | string | yes | The last name of the contact. |
| `data[0].Email` | string | yes | The email address to associate with the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {
          "createdBy": {
            "id": "string",
            "name": "Ava Chen"
          },
          "createdTime": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "modifiedBy": {
            "id": "string",
            "name": "Ava Chen"
          },
          "modifiedTime": "2026-05-07T12:00:00.000Z",
          "tabName": "Ava Chen",
          "uid": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts[].createdBy.id` | string |  |
| `contacts[].createdBy.name` | string |  |
| `contacts[].createdTime` | date |  |
| `contacts[].id` | string |  |
| `contacts[].modifiedBy.id` | string |  |
| `contacts[].modifiedBy.name` | string |  |
| `contacts[].modifiedTime` | date |  |
| `contacts[].tabName` | string |  |
| `contacts[].uid` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `POST /Contacts` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

