# Update Donation Keyword with MojoTxt

Updates a donation keyword in MojoTxt.

## Endpoint

- **Method:** `POST`
- **Path:** `/:phoneNumber/donations/update/:donationIdOrKeyword`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [Update Donation Keyword](https://app.mojotxt.com/api/docs/v1/donations-update.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AmountRequestMessage` | body | `string` | no | Prompt sent when no donation amount is supplied. |
| `CCBFund` | body | `number` | no | Church Community Builder fund number for exports. |
| `DefaultAmount` | body | `number` | no | Default donation amount if the donor does not specify one. |
| `donationIdOrKeyword` | path | `string` | yes | The donation keyword identifier or keyword value to update. |
| `FundName` | body | `string` | no | The updated fund name for the donation keyword. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
| `RecurringScheduleID` | body | `number` | no | Default recurring schedule: 0 one-time, 1 weekly, 2 bi-weekly, 3 monthly, or empty to ask the user. |
| `ThankYou` | body | `string` | no | Thank-you message sent after a successful donation. |
