# Tidio: Create Contact [Plus plan]

Creates a contact in the Tidio workspace.

```
POST https://connect.mindcloud.co/v1/universal/tidio/latest/actions/create-contact-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/create-contact-plus-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "distinctId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidio/latest/actions/create-contact-plus-plan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "distinctId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `distinctId` | string | yes | Custom unique contact identifier. |
| `email` | string | no | Contact email address. |
| `firstName` | string | no | Contact first name. |
| `lastName` | string | no | Contact last name. |
| `phone` | string | no | Contact phone number. |
| `emailConsent` | string | no | Newsletter consent status for the contact. |
| `properties` | list<object> | no | Optional list of custom contact properties. |
| `properties[].name` | string | no | Name of the contact property. |
| `properties[].value` | string | no | Value of the contact property. |

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
| `value` | string |  |

## Native endpoint

Through the native Tidio API, this operation is `POST /contacts` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-plus-plan.md) for the provider-specific parameters and requirements.

