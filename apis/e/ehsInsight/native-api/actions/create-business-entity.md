# Create Business Entity with EHS Insight

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/hierarchy/add`
- **Base URL:** `https://{companyName}.ehsinsight.com/api`
- **Official documentation:** [Create Business Entity](https://qxobptest.ehsinsight.com/openapi/viewer?version=6&category=hierarchy#/Business%20Hierarchy/post_hierarchy_add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
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
| `InstanceHierarchyRevisionList[].EffectiveDate` | body | `date` | no | — |
| `InstanceHierarchyRevisionList[].ParentHierarchyUID` | body | `string` | no | — |
| `InstanceHierarchyRevisionList[].Type` | body | `string` | no | RowUID from the BusinessEntityType entity list. |
| `InstanceHierarchyRevisionList[].SubType` | body | `string` | no | RowUID from the BusinessEntitySubType entity list. |
| `InstanceHierarchyRevisionList[].Client` | body | `string` | no | — |
