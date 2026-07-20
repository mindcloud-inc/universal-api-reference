# Zoho Campaigns: List Mailing Lists

Retrieves mailing lists from Zoho Campaigns.

```
GET https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-mailing-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-mailing-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-mailing-lists?${params}`, {
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
| `sort` | list | no | Sort direction for the returned mailing lists. One of: `asc`, `desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "string",
      "createdTimeGmt": "string",
      "date": "string",
      "deletable": "string",
      "editable": "string",
      "isPublic": "string",
      "issmart": "string",
      "listCampaignsCount": "string",
      "listCreatedDate": "string",
      "listCreatedTime": "string",
      "listdesc": "string",
      "listdgs": "string",
      "listkey": "string",
      "listname": "Ava Chen",
      "listnotifications": "string",
      "listtype": "string",
      "listunino": "string",
      "lockstatus": "string",
      "noofbouncecnt": "string",
      "noofcontacts": "string",
      "noofunsubcnt": "string",
      "otherslist": "string",
      "owner": "string",
      "segments": {},
      "sentcnt": "string",
      "servicetype": "string",
      "sno": "string",
      "updatedTimeGmt": "string",
      "zuid": "string",
      "zx": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | string |  |
| `createdTimeGmt` | string |  |
| `date` | string |  |
| `deletable` | string |  |
| `editable` | string |  |
| `isPublic` | string |  |
| `issmart` | string |  |
| `listCampaignsCount` | string |  |
| `listCreatedDate` | string |  |
| `listCreatedTime` | string |  |
| `listdesc` | string |  |
| `listdgs` | string |  |
| `listkey` | string |  |
| `listname` | string |  |
| `listnotifications` | string |  |
| `listtype` | string |  |
| `listunino` | string |  |
| `lockstatus` | string |  |
| `noofbouncecnt` | string |  |
| `noofcontacts` | string |  |
| `noofunsubcnt` | string |  |
| `otherslist` | string |  |
| `owner` | string |  |
| `segments` | object |  |
| `sentcnt` | string |  |
| `servicetype` | string |  |
| `sno` | string |  |
| `updatedTimeGmt` | string |  |
| `zuid` | string |  |
| `zx` | string |  |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `GET /getmailinglists` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-mailing-lists.md) for the provider-specific parameters and requirements.

