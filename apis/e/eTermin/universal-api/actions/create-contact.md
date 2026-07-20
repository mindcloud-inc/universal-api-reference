# eTermin: Create Contact

Creates a new contact in eTermin.

```
POST https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updatewhenexistsgdt` | number | no | Set to 1 to check if the contact is already existing. If so the existing contact gets updated. Needs email or firstname, lastname, birthday. |
| `salutation` | string | no | Salutation of the person. |
| `title` | string | no | Title of the person. |
| `lastname` | string | no | Lastname of the person. |
| `firstname` | string | no | Firstname of the person. |
| `birthday` | string | no | Birthday of the person. |
| `email` | string | no | E-Mail of the person. |
| `phone` | string | no | Phone of the person. |
| `company` | string | no | Company of the person (make sure this field exists in your account) |
| `street` | string | no | Street of the person. |
| `zip` | string | no | Zip of the person. |
| `city` | string | no | City of the person. |
| `state` | string | no | State of the person. |
| `country` | string | no | Country of the person. |
| `customernumber` | string | no | ID of the person. |
| `loginid` | string | no | Sets the loginID for the contact (if Login is used on Bookingpage). |
| `password` | string | no | Sets the initial password for the contact. |
| `newsletter` | boolean | no | Opts the contact into the newsletter. |
| `additional1` | string | no | Additional appointment field 1. |
| `additional2` | string | no | Additional appointment field 2. |
| `additional3` | string | no | Additional appointment field 3. |
| `additional4` | string | no | Additional appointment field 4. |
| `additional5` | string | no | Additional appointment field 5. |
| `additional6` | string | no | Additional appointment field 6. |
| `additional7` | string | no | Additional appointment field 7. |
| `additional8` | string | no | Additional appointment field 8. |
| `additional9` | string | no | Additional appointment field 9. |
| `additional10` | string | no | Additional appointment field 10. |
| `additional11` | string | no | Additional appointment field 11. |
| `additional12` | string | no | Additional appointment field 12. |
| `additional13` | string | no | Additional appointment field 13. |
| `additional14` | string | no | Additional appointment field 14. |
| `additional15` | string | no | Additional appointment field 15. |
| `additional16` | string | no | Additional appointment field 16. |
| `additional17` | string | no | Additional appointment field 17. |
| `additional18` | string | no | Additional appointment field 18. |
| `additional19` | string | no | Additional appointment field 19. |
| `additional20` | string | no | Additional appointment field 20. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "iid": "string",
      "iide": "string",
      "status": 1,
      "statusMsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `iid` | string |  |
| `iide` | string |  |
| `status` | number |  |
| `statusMsg` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `POST /api/contact` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

