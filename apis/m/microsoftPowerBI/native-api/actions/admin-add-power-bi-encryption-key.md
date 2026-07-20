# Add Power BI Encryption Key with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `admin/tenantKeys`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Add Power BI Encryption Key](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/add-power-bi-encryption-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activate` | body | `boolean` | no | Whether to activate any inactivated capacities and to use this key for its encryption |
| `isDefault` | body | `boolean` | no | Whether an encryption key is the default key for the entire tenant. Any newly created capacity inherits the default key. |
| `keyVaultKeyIdentifier` | body | `string` | no | The URI that uniquely specifies an encryption key in Azure Key Vault |
| `name` | body | `string` | no | The name of the encryption key |
