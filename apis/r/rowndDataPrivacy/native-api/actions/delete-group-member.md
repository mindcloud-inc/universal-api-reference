# Delete Group Member with Rownd Data Privacy

## Endpoint

- **Method:** `DELETE`
- **Path:** `/groups/:group/members/:member`
- **Base URL:** `https://api.rownd.io/applications/{appId}`
- **Official documentation:** [Delete Group Member](https://docs.rownd.io/api-reference/groups/platform/members/member-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `string` | yes | Rownd group identifier. |
| `member` | path | `string` | yes | Rownd group member identifier. |
