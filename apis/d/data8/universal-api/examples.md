# Data8 Universal API Examples

These examples use the MindCloud API key and Data8 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Bank Account

Validates a bank account with Data8.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/data8/latest/actions/validate-bank-account?connectionId=$CONNECTION_ID&sortCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sortCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/data8/latest/actions/validate-bank-account?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "AccountNumber": "string",
      "Address": {
        "RawAddress": {
          "Postcode": "string"
        }
      },
      "BICCode": "string",
      "BranchName": "Ava Chen",
      "FullBankName": "Ava Chen",
      "SortCode": "string",
      "Status": {
        "CreditsRemaining": 1,
        "ErrorMessage": "string",
        "Success": true
      },
      "Valid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate Bank Account action reference](actions/validate-bank-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/data8/latest/actions/validate-bank-account).
