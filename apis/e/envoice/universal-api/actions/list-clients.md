# Envoice: List Clients

Retrieves clients from Envoice.

```
GET https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-clients?${params}`, {
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
      "ClientCountryId": 1,
      "ClientCurrencyId": 1,
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "Email": "ava@example.com",
      "Id": 1,
      "Name": "Ava Chen",
      "UiLanguageId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ClientCountryId` | number | Client country identifier. |
| `ClientCurrencyId` | number | Client currency identifier. |
| `CreatedOn` | date | Client creation timestamp. |
| `Email` | string | Client email address. |
| `Id` | number | Client identifier. |
| `Name` | string | Client name. |
| `UiLanguageId` | number | Client UI language identifier. |

## Native endpoint

Through the native Envoice API, this operation is `GET client/all` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

