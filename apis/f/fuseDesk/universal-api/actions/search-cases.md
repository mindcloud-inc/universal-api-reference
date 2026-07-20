# FuseDesk: Search Cases

Finds cases in FuseDesk by matching search filters.

```
GET https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/search-cases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/search-cases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/search-cases?${params}`, {
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
| `companyId` | string | no |  |
| `contactId` | string | no |  |
| `contactUuid` | string | no |  |
| `createdByRep` | string | no |  |
| `dateAssigned` | string | no |  |
| `dateClosed` | string | no |  |
| `dateFirstResponse` | string | no |  |
| `dateOpened` | string | no |  |
| `dateUpdated` | string | no |  |
| `departmentId` | string | no |  |
| `email` | string | no |  |
| `from` | string | no |  |
| `limit` | string | no |  |
| `offset` | string | no |  |
| `orderBy` | string | no |  |
| `repId` | string | no |  |
| `status` | string | no |  |
| `subject` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "caseid": 1,
      "casenumber": "string",
      "contactUuid": "string",
      "departmentid": 1,
      "details": "string",
      "id": 1,
      "isArchived": true,
      "status": "string",
      "summary": "string",
      "tags": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caseid` | number |  |
| `casenumber` | string |  |
| `contactUuid` | string |  |
| `departmentid` | number |  |
| `details` | string |  |
| `id` | number |  |
| `isArchived` | boolean |  |
| `status` | string |  |
| `summary` | string |  |
| `tags` | array<number> |  |

## Native endpoint

Through the native FuseDesk API, this operation is `GET /api/v1/cases` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-cases.md) for the provider-specific parameters and requirements.

