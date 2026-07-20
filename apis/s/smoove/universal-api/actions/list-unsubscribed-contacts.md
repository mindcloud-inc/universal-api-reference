# Smoove: List Unsubscribed Contacts

Retrieves unsubscribed contacts from Smoove.

```
GET https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-unsubscribed-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smoove `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-unsubscribed-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-unsubscribed-contacts?${params}`, {
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
| `fields` | string | no |  |
| `includeCustomFields` | boolean | no | Default: `false`. |
| `includeLinkedLists` | boolean | no | Default: `false`. |

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
      "timestampSignup": "2026-05-07T12:00:00.000Z"
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

## Native endpoint

Through the native Smoove API, this operation is `GET /v1/Contacts_Unsubscribers` (base URL `https://rest.smoove.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-unsubscribed-contacts.md) for the provider-specific parameters and requirements.

