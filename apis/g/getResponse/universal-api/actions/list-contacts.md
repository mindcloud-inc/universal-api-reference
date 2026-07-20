# GetResponse: List Contacts

Retrieves a list of contacts from GetResponse.

```
GET https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-contacts?${params}`, {
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
| `email` | string | no | Filter contacts by email |
| `name` | string | no | Filter contacts by name |
| `campaignId` | string | no | Filter contacts by campaign |
| `origin` | string | no | Filter contacts by origin |
| `createdOnFrom` | string | no | Return contacts created on or after this date |
| `createdOnTo` | string | no | Return contacts created on or before this date |
| `changedOnFrom` | string | no | Return contacts changed on or after this date |
| `changedOnTo` | string | no | Return contacts changed on or before this date |
| `sortEmail` | string | no | Sort by email order |
| `sortName` | string | no | Sort by name order |
| `sortCreatedOn` | string | no | Sort by creation date order |
| `sortChangedOn` | string | no | Sort by change date order |
| `sortCampaignId` | string | no | Sort by campaign ID order |
| `additionalFlags` | string | no | Additional behavior flags (for example exactMatch) |
| `fields` | string | no | Comma-separated list of fields to return |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string",
      "email": "ava@example.com",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |
| `email` | string |  |
| `name` | string |  |

## Native endpoint

Through the native GetResponse API, this operation is `GET /contacts` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

