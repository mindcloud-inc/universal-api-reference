# Create Proxy Binding with ProxiedMail

## Endpoint

- **Method:** `POST`
- **Path:** `/proxy-bindings`
- **Base URL:** `https://proxiedmail.com/api/v1`
- **Official documentation:** [Create Proxy Binding](https://docs.proxiedmail.com/docs/endpoints/postproxybindings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `proxyAddress` | body | `string` | yes | — |
| `realAddresses` | body | `list<string>` | yes | Send multiple values as a array. |
| `callbackUrl` | body | `string` | no | — |
| `isBrowsable` | body | `boolean` | no | — |
