# MindMe: List Contacts

Retrieves contacts from MindMe.

```
GET https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindMe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/list-contacts?${params}`, {
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
| `contactId` | string | no |  |
| `dateField` | string | no |  |
| `dateFieldFilterIntervalType` | string | no |  |
| `dateFieldIntervalRangeType` | string | no |  |
| `dateIntervalLength` | string | no |  |
| `endDate` | string | no |  |
| `filterBy` | string | no |  |
| `isFilterAfterStartDate` | string | no |  |
| `isFilterByBirthDate` | string | no |  |
| `isFilterByContactUpdateDate` | string | no |  |
| `isFilterByMonth` | string | no |  |
| `listType` | string | no |  |
| `month` | string | no |  |
| `pageNumber` | string | no |  |
| `pageSize` | string | no |  |
| `searchValue` | string | no |  |
| `sortColumnName` | string | no |  |
| `sortingDirection` | string | no |  |
| `sortPreferencePage` | string | no |  |
| `startDate` | string | no |  |
| `typeId` | string | no |  |
| `userId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MindMe API returns.

## Native endpoint

Through the native MindMe API, this operation is `GET /api/Contact/GetContactByFilter` (base URL `https://prodapi.mindmemobile.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

