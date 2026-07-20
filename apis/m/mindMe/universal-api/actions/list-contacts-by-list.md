# MindMe: List Contacts By List

Retrieves contacts from a list in MindMe.

```
GET https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/list-contacts-by-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindMe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/list-contacts-by-list?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/list-contacts-by-list?${params}`, {
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
| `accountId` | string | no |  |
| `birthdayFiltersBySubCategory` | string | no |  |
| `categoryFilterBy` | string | no |  |
| `dateField` | string | no |  |
| `dateFieldFilterIntervalType` | string | no |  |
| `dateFieldIntervalRangeType` | string | no |  |
| `dateIntervalLength` | string | no |  |
| `endDate` | string | no |  |
| `listId` | string | no |  |
| `listType` | string | no |  |
| `pageNumber` | string | no |  |
| `pageSize` | string | no |  |
| `searchValue` | string | no |  |
| `sortColumnName` | string | no |  |
| `sortingDirection` | string | no |  |
| `startDate` | string | no |  |
| `typeId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MindMe API returns.

## Native endpoint

Through the native MindMe API, this operation is `GET /api/List/GetContactsByList` (base URL `https://prodapi.mindmemobile.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts-by-list.md) for the provider-specific parameters and requirements.

