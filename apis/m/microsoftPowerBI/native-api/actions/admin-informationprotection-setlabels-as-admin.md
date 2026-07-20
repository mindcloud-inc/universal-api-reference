# InformationProtection SetLabelsAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `admin/informationprotection/setLabels`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [InformationProtection SetLabelsAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/information-protection-set-labels-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `artifacts` | body | `object` | yes | A composite of Power BI item IDs for each item type |
| `labelId` | body | `string` | yes | The label ID, which must be in the user's label policy. |
| `assignmentMethod` | body | `object` | no | Specifies whether the assigned label was set by an automated process or manually. |
| `delegatedUser` | body | `object` | no | Delegated user details. A delegated user is a user within an organization whose admin sets a label on behalf of the user. Although the admin sets the label, the delegated user is marked as the label issuer. |
