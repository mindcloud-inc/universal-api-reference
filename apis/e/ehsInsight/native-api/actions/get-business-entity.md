# Get Business Entity with EHS Insight

## Endpoint

- **Method:** `GET`
- **Path:** `/v6/hierarchy/fetch/:rowUid`
- **Base URL:** `https://{companyName}.ehsinsight.com/api`
- **Official documentation:** [Get Business Entity](https://qxobptest.ehsinsight.com/openapi/viewer?version=6&category=hierarchy#/Business%20Hierarchy/get_hierarchy_fetch__RowUID_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rowUid` | path | `string` | yes | The RowUID of the Business Entity to fetch, including all revisions. |
