# Delete Donation with MojoTxt

Deletes a donation from MojoTxt.

## Endpoint

- **Method:** `POST`
- **Path:** `/:phoneNumber/donations/delete/:donationIdOrKeyword`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [Delete Donation](https://app.mojotxt.com/api/docs/v1/donations-delete.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `donationIdOrKeyword` | path | `string` | yes | The donation keyword identifier or keyword value to delete. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
