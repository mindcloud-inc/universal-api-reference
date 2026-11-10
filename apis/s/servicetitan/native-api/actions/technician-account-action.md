# Technician Account Action with ServiceTitan

## Endpoint

- **Method:** `POST`
- **Path:** `settings/v2/tenant/{tenant}/technicians/:id/account-actions`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Technician Account Action](https://developer.servicetitan.io/docs/apis/tenant-settings-v2/endpoints/Technicians_AccountActions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ServiceTitan technician ID. |
| `action` | body | `list<string>` | yes | Account action to perform: Activate, Deactivate, SendInvite, or SendPasswordResetLink. Accepted values: `Activate`, `Deactivate`, `SendInvite`, `SendPasswordResetLink`. |
| `licenseType` | body | `list<string>` | no | License type to assign to the technician. Required when Action = Activate. Accepted values: `ManagedInstaller`, `ManagedTechnician`, `NonManagedTechnician`. |
| `truckId` | body | `number` | no | (Optional) Truck ID to assign to the technician. |
