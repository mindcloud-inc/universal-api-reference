# Get a Newsletter: List Contacts

Lists contacts in Get a Newsletter.

```
GET https://connect.mindcloud.co/v1/universal/getANewsletter/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Get a Newsletter `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getANewsletter/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getANewsletter/latest/actions/list-contacts?${params}`, {
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
| `page` | number | no |  |
| `ordering` | string | no |  |
| `searchEmail` | string | no |  |
| `searchName` | string | no |  |
| `lists[]` | array<string> | no |  |
| `updatedLt` | date | no |  |
| `updatedGt` | date | no |  |
| `updatedYear` | number | no |  |
| `updatedMonth` | number | no |  |
| `updatedDay` | number | no |  |
| `createdLt` | date | no |  |
| `createdGt` | date | no |  |
| `createdYear` | number | no |  |
| `createdMonth` | number | no |  |
| `createdDay` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Get a Newsletter API returns.

## Native endpoint

Through the native Get a Newsletter API, this operation is `GET /contacts/` (base URL `https://api.getanewsletter.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

