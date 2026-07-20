# Get Donation with MojoTxt

Retrieves a donation from MojoTxt.

## Endpoint

- **Method:** `GET`
- **Path:** `/:phoneNumber/donations/get/:donationIdOrKeyword`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [Get Donation](https://app.mojotxt.com/api/docs/v1/donations-get.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `donationIdOrKeyword` | path | `string` | yes | The donation keyword identifier or keyword value to retrieve. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
