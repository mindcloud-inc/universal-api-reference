# MojoTxt: List Donations

Retrieves donations for a MojoTxt phone number.

```
GET https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-donations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-donations?connectionId=$CONNECTION_ID&limit=25&offset=0&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-donations?${params}`, {
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
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |
| `stats` | string | no | Set to 1 to include donation statistics in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CCBFund": 1,
      "DefaultAmount": 1,
      "DonationID": 1,
      "FundName": "Ava Chen",
      "Keyword": "string",
      "LastDonationTime": 1,
      "RecurringScheduleID": 1,
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
| `CCBFund` | number | The optional Church Community Builder fund number. |
| `DefaultAmount` | number | The default donation amount, if configured. |
| `DonationID` | number | The unique identifier for the donation keyword. |
| `FundName` | string | The name of the donation fund. |
| `Keyword` | string | The keyword donors use for the donation fund. |
| `LastDonationTime` | number | The UNIX timestamp of the latest donation when stats are included. |
| `RecurringScheduleID` | number | The default recurring donation schedule identifier. |
| `TotalAmountDonated` | number | The total amount donated through this keyword when stats are included. |
| `TotalDonations` | number | The total number of donations through this keyword when stats are included. |

## Native endpoint

Through the native MojoTxt API, this operation is `GET /:phoneNumber/donations/list` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-donations.md) for the provider-specific parameters and requirements.

