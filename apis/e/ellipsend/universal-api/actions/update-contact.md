# Ellipsend: Update Contact

Updates a contact in Ellipsend by token.

```
PUT https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ellipsend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "token": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "token": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `token` | string | yes | The contact token. |
| `statusId` | number | no | ID of the status to assign. |
| `labelId` | number | no | ID of the label to assign. |
| `assigneeId` | number | no | ID of the assignee to assign. |
| `firstName` | string | no | Contact's first name. |
| `lastName` | string | no | Contact's last name. |
| `email` | string | no | Contact's email address. |
| `phone` | string | no | Contact's phone number. |
| `address` | string | no | Contact's physical address. |
| `city` | string | no | Contact's city. |
| `state` | string | no | Contact's state or province. |
| `postalCode` | string | no | Contact's postal or zip code. |
| `country` | string | no | Contact's country. |
| `company` | string | no | Contact's company name. |
| `title` | string | no | Contact's job title. |
| `customFields` | object | no | Additional custom fields for the contact. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ellipsend API returns.

## Native endpoint

Through the native Ellipsend API, this operation is `PUT /contact/[:token]` (base URL `https://api.ellipsend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

