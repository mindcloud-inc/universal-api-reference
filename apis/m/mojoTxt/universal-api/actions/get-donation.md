# MojoTxt: Get Donation

Retrieves a donation from MojoTxt.

```
GET https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/get-donation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/get-donation?connectionId=$CONNECTION_ID&donationIdOrKeyword=string&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "donationIdOrKeyword": "string",
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/get-donation?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `donationIdOrKeyword` | string | yes | The donation keyword identifier or keyword value to retrieve. |
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AmountRequestMessage": "string",
      "CCBFund": 1,
      "DefaultAmount": 1,
      "DonationID": 1,
      "FundName": "Ava Chen",
      "Keyword": "string",
      "KeywordID": 1,
      "LastDonationTime": 1,
      "Listed": 1,
      "NumberOfDonors": 1,
      "RecurringScheduleID": 1,
      "ThankYou": "string",
      "TotalAmountDonated": 1,
      "TotalDonations": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AmountRequestMessage` | string | The amount prompt shown when donors omit a value. |
| `CCBFund` | number | The optional Church Community Builder fund number. |
| `DefaultAmount` | number | The default donation amount, if configured. |
| `DonationID` | number | The unique identifier for the donation keyword. |
| `FundName` | string | The name of the donation fund. |
| `Keyword` | string | The keyword donors use for the donation fund. |
| `KeywordID` | number | The keyword identifier associated with the donation keyword. |
| `LastDonationTime` | number | The UNIX timestamp of the latest donation. |
| `Listed` | number | Whether the donation keyword is active and listed. |
| `NumberOfDonors` | number | The number of unique donors for this keyword. |
| `RecurringScheduleID` | number | The default recurring donation schedule identifier. |
| `ThankYou` | string | The thank-you message sent after a donation. |
| `TotalAmountDonated` | number | The total amount donated through this keyword. |
| `TotalDonations` | number | The total number of donations through this keyword. |

## Native endpoint

Through the native MojoTxt API, this operation is `GET /:phoneNumber/donations/get/:donationIdOrKeyword` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-donation.md) for the provider-specific parameters and requirements.

