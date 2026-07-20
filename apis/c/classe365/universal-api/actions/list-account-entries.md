# Classe365: List Account Entries

Retrieves a list of account entries from Classe365.

```
GET https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-account-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-account-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-account-entries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "entryId": 1,
      "ledgerAccountId": 1,
      "transactionDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `entryId` | number |  |
| `ledgerAccountId` | number |  |
| `transactionDate` | date |  |

## Native endpoint

Through the native Classe365 API, this operation is `GET /rest/accountEntries` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-entries.md) for the provider-specific parameters and requirements.

