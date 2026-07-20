# Tidio: Update Multiple Contacts [Plus plan]

Updates multiple contacts in the Tidio workspace.

```
PUT https://connect.mindcloud.co/v1/universal/tidio/latest/actions/update-multiple-contacts-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/update-multiple-contacts-plus-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts": {},
  "contacts[].id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidio/latest/actions/update-multiple-contacts-plus-plan', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts": {},
    "contacts[].id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts` | list<object> | yes | List of contacts to update. Maximum 100 per request. |
| `contacts[].id` | string | yes | Tidio contact UUID to update. |
| `contacts[].distinctId` | string | no | External-system identifier for the contact. |
| `contacts[].email` | string | no | Contact email address. |
| `contacts[].firstName` | string | no | Contact first name. |
| `contacts[].lastName` | string | no | Contact last name. |
| `contacts[].phone` | string | no | Contact phone number. |
| `contacts[].emailConsent` | string | no | Newsletter consent status for the contact. |
| `contacts[].properties` | list<object> | no | Optional list of custom contact properties. |
| `contacts[].properties[].name` | string | no | Name of the contact property. |
| `contacts[].properties[].value` | string | no | Value of the contact property. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. Tidio docs specify 204 It means that all the contacts have been updated.. |

## Native endpoint

Through the native Tidio API, this operation is `PATCH /contacts/batch` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-multiple-contacts-plus-plan.md) for the provider-specific parameters and requirements.

