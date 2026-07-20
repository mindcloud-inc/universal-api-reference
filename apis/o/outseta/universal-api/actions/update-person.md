# Outseta: Update Person

Updates an existing person in Outseta.

```
PUT https://connect.mindcloud.co/v1/universal/outseta/latest/actions/update-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/update-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "personUid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/update-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "personUid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `personUid` | string | yes |  |
| `email` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `mailingAddress.uid` | string | no |  |
| `mailingAddress.addressLine1` | string | no |  |
| `mailingAddress.addressLine2` | string | no |  |
| `mailingAddress.addressLine3` | string | no |  |
| `mailingAddress.city` | string | no |  |
| `mailingAddress.state` | string | no |  |
| `mailingAddress.postalCode` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Created": "string",
      "Email": "ava@example.com",
      "FirstName": "Ava",
      "FullName": "Ava Chen",
      "LastName": "Chen",
      "Uid": "string",
      "Updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Created` | string |  |
| `Email` | string |  |
| `FirstName` | string |  |
| `FullName` | string |  |
| `LastName` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `PUT /crm/people/:personUid` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person.md) for the provider-specific parameters and requirements.

