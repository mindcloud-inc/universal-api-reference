# Create Donation Keyword with MojoTxt

Creates a donation keyword in MojoTxt.

## Endpoint

- **Method:** `POST`
- **Path:** `/:phoneNumber/donations/add`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [Create Donation Keyword](https://app.mojotxt.com/api/docs/v1/donations-add.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AmountRequestMessage` | body | `string` | no | Prompt sent when no donation amount is supplied. |
| `CCBFund` | body | `number` | no | Church Community Builder fund number for exports. |
| `DefaultAmount` | body | `number` | no | Default donation amount if the donor does not specify one. |
| `FundName` | body | `string` | no | Fund name for the donation keyword. MojoTxt currently defaults this when omitted, despite the docs marking it required. |
| `Keyword` | body | `string` | yes | The unique keyword for the donation fund. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
| `RecurringScheduleID` | body | `number` | no | Default recurring schedule: 0 one-time, 1 weekly, 2 bi-weekly, 3 monthly, or empty to ask the user. |
| `ThankYou` | body | `string` | no | Thank-you message sent after a successful donation. |
