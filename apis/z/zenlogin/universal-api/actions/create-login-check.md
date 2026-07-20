# Zenlogin: Create Login Check



```
POST https://connect.mindcloud.co/v1/universal/zenlogin/latest/actions/create-login-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenlogin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zenlogin/latest/actions/create-login-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identityKey": "usr12345",
  "identityEmailAddress": "name@example.com",
  "userAgent": "Mozilla/5.0",
  "ipAddress": "20.169.78.172"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenlogin/latest/actions/create-login-check', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identityKey": "usr12345",
    "identityEmailAddress": "name@example.com",
    "userAgent": "Mozilla/5.0",
    "ipAddress": "20.169.78.172"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identityKey` | string | yes | Stable unique identifier for the user being checked. Zenlogin recommends this should not be the user's email address. Maximum length is 128 characters. Example: `usr12345`. |
| `identityEmailAddress` | string | yes | Email address Zenlogin can notify if a suspicious login is detected. Maximum length is 256 characters. Example: `name@example.com`. |
| `userAgent` | string | yes | User agent observed during the login attempt. Maximum length is 512 characters. Example: `Mozilla/5.0`. |
| `ipAddress` | string | yes | IP address observed during the login attempt. Official examples use the `ip_address` payload field. Maximum length is 256 characters. Example: `20.169.78.172`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identityFirstName` | string | no | Optional first name for notification template variables. Maximum length is 256 characters. |
| `identityLastName` | string | no | Optional last name for notification template variables. Maximum length is 256 characters. |
| `identityFullName` | string | no | Optional full name for notification template variables. Maximum length is 256 characters. |
| `reqProcess` | number | no | Optional 0 or 1 flag controlling whether Zenlogin should process this login check. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "email_notification_sent": 1,
        "id": "string",
        "status_key": "string",
        "timestamp": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | JSON:API data object returned by Zenlogin. |
| `data.email_notification_sent` | number | Whether Zenlogin sent an email notification for the login check. Runtime not-processed checks returned 0. |
| `data.id` | string | Unique ID associated with the login check when Zenlogin processes the request; not-processed runtime checks may return null. |
| `data.status_key` | string | Status key returned by Zenlogin for the login check, such as not_processed when req_process is 0. |
| `data.timestamp` | number | Unix timestamp when Zenlogin received the API request. |

## Native endpoint

Through the native Zenlogin API, this operation is `POST /applications/[:application_key]/logins/checks` (base URL `https://api.zenlogin.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-login-check.md) for the provider-specific parameters and requirements.

