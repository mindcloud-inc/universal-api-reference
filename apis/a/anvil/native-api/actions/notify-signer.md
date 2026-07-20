# Notify Signer with Anvil

Notifies a signer by email in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Notify Signer](https://www.useanvil.com/docs/api/graphql/reference/#mutation-notifySigner)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.signerEid` | body | `string` | yes | Provide Signer EID for Notify Signer. |
