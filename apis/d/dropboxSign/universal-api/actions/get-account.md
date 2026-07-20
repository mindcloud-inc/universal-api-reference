# Dropbox Sign: Get Account

Retrieves your Dropbox Sign account settings.

```
GET https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-account?${params}`, {
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
| `accountId` | string | no | The ID of the account to retrieve. If both Account ID and Email Address are provided, Account ID wins. |
| `emailAddress` | string | no | The email address of the account to retrieve when Account ID is not provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "callbackUrl": {},
      "emailAddress": "ava@example.com",
      "isLocked": true,
      "isPaidHf": true,
      "isPaidHs": true,
      "locale": "string",
      "quotas": {
        "apiSignatureRequestsLeft": 1,
        "documentsLeft": 1,
        "templatesLeft": 1,
        "templatesTotal": 1
      },
      "roleCode": {},
      "settings": {
        "signerAccessCodes": true,
        "smsAuthentication": true,
        "smsDelivery": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `callbackUrl` | object |  |
| `emailAddress` | string |  |
| `isLocked` | boolean |  |
| `isPaidHf` | boolean |  |
| `isPaidHs` | boolean |  |
| `locale` | string |  |
| `quotas.apiSignatureRequestsLeft` | number |  |
| `quotas.documentsLeft` | number |  |
| `quotas.templatesLeft` | number |  |
| `quotas.templatesTotal` | number |  |
| `roleCode` | object |  |
| `settings.signerAccessCodes` | boolean |  |
| `settings.smsAuthentication` | boolean |  |
| `settings.smsDelivery` | boolean |  |

## Native endpoint

Through the native Dropbox Sign API, this operation is `GET /account` (base URL `https://api.hellosign.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

