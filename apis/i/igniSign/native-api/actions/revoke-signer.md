# Revoke Signer with IgniSign

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v4/applications/:appId/envs/:appEnv/signers/:signerId/revoke`
- **Base URL:** `https://api.ignisign.io`
- **Official documentation:** [Revoke Signer](https://ignisign.io/docs/ignisign-api/signers/revoke-a-signer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signerId` | path | `string` | yes | The IgniSign signer ID. |
