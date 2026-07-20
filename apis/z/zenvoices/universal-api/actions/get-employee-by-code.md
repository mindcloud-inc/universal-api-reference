# Zenvoices: Get Employee By Code

Retrieves an employee from Zenvoices by code.

```
GET https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-employee-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenvoices `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-employee-by-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-employee-by-code?${params}`, {
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
      "administrationId": 1,
      "code": "string",
      "costCentreCode": "string",
      "externalId": "string",
      "externalLastModificationTime": "2026-05-07T12:00:00.000Z",
      "fullName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrationId` | number | administrationId returned by Zenvoices. |
| `code` | string | code returned by Zenvoices. |
| `costCentreCode` | string | costCentreCode returned by Zenvoices. |
| `externalId` | string | externalId returned by Zenvoices. |
| `externalLastModificationTime` | date | externalLastModificationTime returned by Zenvoices. |
| `fullName` | string | fullName returned by Zenvoices. |

## Native endpoint

Through the native Zenvoices API, this operation is `GET /public-api/v1/employees` (base URL `https://app.zenvoices.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-by-code.md) for the provider-specific parameters and requirements.

