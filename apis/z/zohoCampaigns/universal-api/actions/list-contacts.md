# Zoho Campaigns: List Contacts

Retrieves contacts from a Zoho Campaigns list.

```
GET https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&listkey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "listkey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-contacts?${params}`, {
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
| `listkey` | list<string> | yes | Mailing list key to read contacts from. |
| `sort` | list<string> | no | Sort direction for the returned contacts. One of: `asc`, `desc`. |
| `status` | list<string> | no | Contact status bucket to include in the results. One of: `active`, `bounce`, `mostrecent`, `recent`, `unsub`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedTime": "string",
      "companyname": "Ava Chen",
      "contactEmail": "ava@example.com",
      "firstname": "Ava",
      "lastname": "Chen",
      "phone": "string",
      "zuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedTime` | string |  |
| `companyname` | string |  |
| `contactEmail` | string |  |
| `firstname` | string |  |
| `lastname` | string |  |
| `phone` | string |  |
| `zuid` | string |  |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `GET /getlistsubscribers` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

