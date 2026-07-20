# Tidio: Update Contact Properties [Plus plan]

Updates a contact in the Tidio workspace.

```
PUT https://connect.mindcloud.co/v1/universal/tidio/latest/actions/update-contact-properties-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/update-contact-properties-plus-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidio/latest/actions/update-contact-properties-plus-plan', {
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
| `contactId` | string | yes | The Tidio contact ID. |
| `email` | string | no | Contact email address. |
| `firstName` | string | no | Contact first name. |
| `lastName` | string | no | Contact last name. |
| `phone` | string | no | Contact phone number. |
| `emailConsent` | string | no | Newsletter consent status for the contact. |
| `distinctId` | string | no | Custom unique contact identifier. |
| `properties` | list<object> | no | Optional list of custom contact properties to patch. |
| `properties[].name` | string | no | Name of the contact property. |
| `properties[].value` | string | no | Value of the contact property. Leave empty when clearing the value upstream. |

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
| `value` | string | The raw response body. Tidio docs specify 204 It means that the contact has been updated.. |

## Native endpoint

Through the native Tidio API, this operation is `PATCH /contacts/{contactId}` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-properties-plus-plan.md) for the provider-specific parameters and requirements.

