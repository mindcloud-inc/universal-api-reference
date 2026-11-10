# EHS Insight: Create Business Entity



```
POST https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/create-business-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EHS Insight `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/create-business-entity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/create-business-entity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no |  |
| `startDate` | date | no | For sites with Business Entity Revisions disabled. Use the effective date on revisions when revisions are enabled. Example: `2026-01-15`. |
| `parentHierarchyUid` | string | no | For sites with revisions disabled; otherwise set the parent on each revision. |
| `type` | string | no | RowUID from the BusinessEntityType entity list. |
| `subType` | string | no | RowUID from the BusinessEntitySubType entity list. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | no |  |
| `endDate` | date | no | Example: `2026-01-15`. |
| `client` | string | no | Client reference, when supported by the site's Business Entity configuration. |
| `comments` | string | no |  |
| `latLong` | string | no |  |
| `instanceHierarchyRevisionList[]` | array<object> | no | For sites with Business Entity Revisions enabled. Supply the revisions instead of the root Start Date, Parent Hierarchy UID, Type, Sub Type, and Client fields. |
| `instanceHierarchyRevisionList[].effectiveDate` | date | no | Example: `2026-01-15`. |
| `instanceHierarchyRevisionList[].parentHierarchyUid` | string | no |  |
| `instanceHierarchyRevisionList[].type` | string | no | RowUID from the BusinessEntityType entity list. |
| `instanceHierarchyRevisionList[].subType` | string | no | RowUID from the BusinessEntitySubType entity list. |
| `instanceHierarchyRevisionList[].client` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EHS Insight API returns.

## Native endpoint

Through the native EHS Insight API, this operation is `POST /v6/hierarchy/add` (base URL `https://{{credentials.companyName}}.ehsinsight.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-business-entity.md) for the provider-specific parameters and requirements.

