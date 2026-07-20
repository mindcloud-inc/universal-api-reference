# Better Proposals: Get Custom Merge Tags

Retrieves custom merge tags from Better Proposals.

```
GET https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-custom-merge-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-custom-merge-tags?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-custom-merge-tags?${params}`, {
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
| `page` | number | no | Page number. Default: 1. Default: `1`. |
| `perPage` | number | no | Results per page. Default: 10. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountID": "string",
      "archived": "string",
      "archivedBy": {},
      "createdBy": "string",
      "cRMSync": "string",
      "cRMTagId": {},
      "cRMTagName": {},
      "dateArchived": "2026-05-07T12:00:00.000Z",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateEdited": "2026-05-07T12:00:00.000Z",
      "editedBy": {},
      "fallback": "string",
      "id": "string",
      "name": "Ava Chen",
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountID` | string |  |
| `archived` | string |  |
| `archivedBy` | object |  |
| `createdBy` | string |  |
| `cRMSync` | string |  |
| `cRMTagId` | object |  |
| `cRMTagName` | object |  |
| `dateArchived` | date |  |
| `dateCreated` | date |  |
| `dateEdited` | date |  |
| `editedBy` | object |  |
| `fallback` | string |  |
| `id` | string |  |
| `name` | string |  |
| `tag` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `GET /settings/merge_tag` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-custom-merge-tags.md) for the provider-specific parameters and requirements.

