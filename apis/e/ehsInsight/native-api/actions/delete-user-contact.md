# Delete User Contact with EHS Insight

## Endpoint

- **Method:** `GET`
- **Path:** `/v6/entity/UserContact/delete/:rowUid`
- **Base URL:** `https://{companyName}.ehsinsight.com/api`
- **Official documentation:** [Delete User Contact](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_entityapi_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rowUid` | path | `string` | yes | The RowUID of the user or contact to delete. Obtain it from List User Contacts with Parameters or Get User Contact. |
