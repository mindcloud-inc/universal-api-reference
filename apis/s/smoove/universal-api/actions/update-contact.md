# Smoove: Update Contact

Updates an existing contact in Smoove by identifier.

```
PUT https://connect.mindcloud.co/v1/universal/smoove/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smoove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smoove/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `by` | list | no | One of: `CellPhone`, `ContactId`, `Email`, `ExternalId`. Default: `ContactId`. |
| `email` | string | no |  |
| `externalId` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `cellPhone` | string | no |  |
| `phone` | string | no |  |
| `password` | string | no |  |
| `dateOfBirth` | date | no |  |
| `address` | string | no |  |
| `city` | string | no |  |
| `country` | string | no |  |
| `company` | string | no |  |
| `position` | string | no |  |
| `canReceiveEmails` | boolean | no | Default: `true`. |
| `canReceiveSmsMessages` | boolean | no | Default: `true`. |
| `listsToSubscribe[]` | array<number> | no |  |
| `listsToUnsubscribe[]` | array<number> | no |  |
| `customFields` | object | no |  |
| `options` | object | no |  |
| `campaignSource` | string | no |  |
| `restoreIfDeleted` | boolean | no | Default: `false`. |
| `restoreIfUnsubscribed` | boolean | no | Default: `false`. |
| `overrideNullableValue` | boolean | no | Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "c_DaysSinceSignup": 1,
      "campaignSource": "string",
      "canReceiveEmails": true,
      "canReceiveSmsMessages": true,
      "cellPhone": "string",
      "city": "string",
      "company": "string",
      "country": "string",
      "dateOfBirth": "2026-05-07T12:00:00.000Z",
      "deleted": true,
      "email": "ava@example.com",
      "externalId": "string",
      "firstName": "Ava",
      "id": 1,
      "ipSignup": "string",
      "joinSource": "string",
      "lastChanged": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "listAssociationTime": "2026-05-07T12:00:00.000Z",
      "phone": "string",
      "position": "string",
      "timestampSignup": "2026-05-07T12:00:00.000Z",
      "timestampUnsubscribed": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `c_DaysSinceSignup` | number |  |
| `campaignSource` | string |  |
| `canReceiveEmails` | boolean |  |
| `canReceiveSmsMessages` | boolean |  |
| `cellPhone` | string |  |
| `city` | string |  |
| `company` | string |  |
| `country` | string |  |
| `dateOfBirth` | date |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `externalId` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `ipSignup` | string |  |
| `joinSource` | string |  |
| `lastChanged` | date |  |
| `lastName` | string |  |
| `listAssociationTime` | date |  |
| `phone` | string |  |
| `position` | string |  |
| `timestampSignup` | date |  |
| `timestampUnsubscribed` | date |  |

## Native endpoint

Through the native Smoove API, this operation is `PUT /v1/Contacts/:id` (base URL `https://rest.smoove.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

