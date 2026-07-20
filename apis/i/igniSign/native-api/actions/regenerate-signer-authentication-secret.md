# Regenerate Signer Authentication Secret with IgniSign

## Endpoint

- **Method:** `PUT`
- **Path:** `/v4/applications/:appId/envs/:appEnv/signers/:signerId/regenerate-auth-secret`
- **Base URL:** `https://api.ignisign.io`
- **Official documentation:** [Regenerate Signer Authentication Secret](https://ignisign.io/docs/ignisign-api/signers/regenerate-signer-authentication-secret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signerId` | path | `string` | yes | The IgniSign signer ID. |
