# Raisely: List Subscription Donations

Retrieves donations from a Raisely subscription.

```
GET https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-subscription-donations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-subscription-donations?connectionId=$CONNECTION_ID&limit=25&offset=0&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-subscription-donations?${params}`, {
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
| `uuid` | string | yes | The `uuid` of the record |
| `private` | boolean | no | Returns the full record when authenticated |
| `q` | string | no | Search query to find records matching |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | no | Filter Donation based on their type value |
| `currency` | string | no | Filter Donation based on their currency value |
| `isSuspicious` | boolean | no | Filter Donation based on their isSuspicious value |
| `status` | string | no | Filter Donation based on their status value |
| `mode` | string | no | Filter Donation based on their mode value |
| `user` | string | no | Filter by user uuid |
| `campaign` | string | no | Filter by campaign path or uuid |
| `organisation` | string | no | Filter by organisation uuid |
| `profile` | string | no | Filter by profile path or uuid |
| `subscription` | string | no | Filter by subscription uuid |
| `matchedDonationConfig` | string | no | Filter by matched donation config path or uuid |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "anonymous": true,
      "campaignUuid": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "email": "ava@example.com",
      "fee": 1,
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "lastName": "Chen",
      "message": "string",
      "method": "string",
      "mode": "string",
      "preferredName": "Ava Chen",
      "profileUuid": "string",
      "publicAmount": 1,
      "publicFee": 1,
      "status": "string",
      "subscriptionUuid": "string",
      "total": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userUuid": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `anonymous` | boolean |  |
| `campaignUuid` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `email` | string |  |
| `fee` | number |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `message` | string |  |
| `method` | string |  |
| `mode` | string |  |
| `preferredName` | string |  |
| `profileUuid` | string |  |
| `publicAmount` | number |  |
| `publicFee` | number |  |
| `status` | string |  |
| `subscriptionUuid` | string |  |
| `total` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userUuid` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Raisely API, this operation is `GET /subscriptions/:uuid/donations` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscription-donations.md) for the provider-specific parameters and requirements.

