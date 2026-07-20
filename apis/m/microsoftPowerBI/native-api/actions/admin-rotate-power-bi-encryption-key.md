# Rotate Power BI Encryption Key with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `admin/tenantKeys/[:tenantKeyId]/Default.Rotate`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Rotate Power BI Encryption Key](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/rotate-power-bi-encryption-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenantKeyId` | path | `string` | yes | The tenant key ID |
| `keyVaultKeyIdentifier` | body | `string` | no | The URI that uniquely specifies the encryption key in Azure Key Vault |
