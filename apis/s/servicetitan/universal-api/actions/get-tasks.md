# ServiceTitan: Get Tasks



```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-tasks?${params}`, {
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
| `name` | string | no |  |
| `projectId` | string | no |  |
| `ids` | string | no |  |
| `statuses` | string | no |  |
| `active` | string | no |  |
| `customerId` | string | no |  |
| `includeSubtacks` | boolean | no |  |
| `jobId` | string | no |  |
| `createdOnOrAfter` | string | no |  |
| `modifiedOnOrAfter` | string | no |  |
| `employeeTaskResolutionIds` | string | no |  |
| `taskNumber` | string | no |  |
| `createdBefore` | string | no |  |
| `modifiedBefore` | string | no |  |
| `reportedBefore` | string | no |  |
| `reportedOnOrAfter` | string | no |  |
| `businessUnitIds` | string | no |  |
| `jobNumber` | string | no |  |
| `sort` | string | no | Applies sorting by the specified field: "?sort=+FieldName" for ascending order, "?sort=-FieldName" for descending order. Available fields are: Id, CreatedOn, DescriptionModifiedOn, CompletedBy, Priority |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `GET taskmanagement/v2/tenant/{{credentials.tenant}}/tasks` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-tasks.md) for the provider-specific parameters and requirements.

