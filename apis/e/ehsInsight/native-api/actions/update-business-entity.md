# Update Business Entity with EHS Insight

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/hierarchy/update`
- **Base URL:** `https://{companyName}.ehsinsight.com/api`
- **Official documentation:** [Update Business Entity](https://qxobptest.ehsinsight.com/openapi/viewer?version=6&category=hierarchy#/Business%20Hierarchy/post_hierarchy_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `RowUID` | body | `string` | yes | RowUID from Get Business Entity. |
| `ChangeToken` | body | `string` | yes | Use the unchanged ChangeToken returned by Get Business Entity to protect against conflicting updates. |
| `Title` | body | `string` | no | — |
| `ExternalID` | body | `string` | no | — |
| `StartDate` | body | `date` | no | For sites with Business Entity Revisions disabled. Use the effective date on revisions when revisions are enabled. |
| `EndDate` | body | `date` | no | — |
| `ParentHierarchyUID` | body | `string` | no | For sites with revisions disabled; otherwise set the parent on each revision. |
| `Type` | body | `string` | no | RowUID from the BusinessEntityType entity list. |
| `SubType` | body | `string` | no | RowUID from the BusinessEntitySubType entity list. |
| `Client` | body | `string` | no | Client reference, when supported by the site's Business Entity configuration. |
| `Comments` | body | `string` | no | — |
| `LatLong` | body | `string` | no | — |
| `InstanceHierarchyRevisionList[]` | body | `array<object>` | no | For sites with Business Entity Revisions enabled. Supply the revisions instead of the root Start Date, Parent Hierarchy UID, Type, Sub Type, and Client fields. |
| `InstanceHierarchyRevisionList[].RowUID` | body | `string` | no | Preserve the RowUID of every existing revision returned by Get Business Entity. |
| `InstanceHierarchyRevisionList[].EffectiveDate` | body | `date` | no | — |
| `InstanceHierarchyRevisionList[].ParentHierarchyUID` | body | `string` | no | — |
| `InstanceHierarchyRevisionList[].Type` | body | `string` | no | RowUID from the BusinessEntityType entity list. |
| `InstanceHierarchyRevisionList[].SubType` | body | `string` | no | RowUID from the BusinessEntitySubType entity list. |
| `InstanceHierarchyRevisionList[].Client` | body | `string` | no | — |
