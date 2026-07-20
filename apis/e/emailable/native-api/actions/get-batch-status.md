# Get Batch Status with Emailable

Retrieves the status of a batch from Emailable.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/batch`
- **Base URL:** `https://api.emailable.com`
- **Official documentation:** [Get Batch Status](https://emailable.com/docs/api/#get-the-status-of-a-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The batch ID returned when you created the verification batch. |
| `partial` | query | `boolean` | no | Set to true to include partial results while a batch of up to 1,000 emails is still verifying. |
