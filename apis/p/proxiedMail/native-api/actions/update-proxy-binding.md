# Update Proxy Binding with ProxiedMail

## Endpoint

- **Method:** `PATCH`
- **Path:** `/proxy-bindings/:proxyBindingId`
- **Base URL:** `https://proxiedmail.com/api/v1`
- **Official documentation:** [Update Proxy Binding](https://docs.proxiedmail.com/docs/endpoints/patchproxybindings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `proxyBindingId` | path | `string` | yes | — |
| `proxyAddress` | body | `string` | no | — |
| `realAddresses` | body | `list<string>` | no | Send multiple values as a array. |
| `description` | body | `string` | no | — |
| `callbackUrl` | body | `string` | no | — |
| `isBrowsable` | body | `boolean` | no | — |
