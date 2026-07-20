# Create Setup Fee with Payfunnels

Creates a new setup fee in Payfunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/fees/setup`
- **Base URL:** `https://api.payfunnels.com`
- **Official documentation:** [Create Setup Fee](https://api.payfunnels.com/api/docs/#create-one-time-setup-fees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Amount to charge for the setup fee. |
| `currency` | body | `string` | yes | Currency code for the setup fee. |
| `name` | body | `string` | yes | Name of the setup fee. |
| `setAsDefault` | body | `boolean` | no | Set true to mark this setup fee as the default. |
