# Clearout: Find Email Instantly

Finds contact email addresses in Clearout instantly.

```
GET https://connect.mindcloud.co/v1/universal/clearout/latest/actions/find-email-instantly
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clearout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/find-email-instantly?connectionId=$CONNECTION_ID&name=Ava%20Chen&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearout/latest/actions/find-email-instantly?${params}`, {
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
| `name` | string | yes | Name of the person (eg:- Mr. Tony Stark or Robert Downey Jr.) |
| `domain` | string | yes | Domain or Company name (eg:- marvel.com or Marvel Entertainment Company) |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeout` | number | no | Request wait time (in milliseconds) Default: `30000`. |
| `queue` | boolean | no | Flag to indicate whether email discovery can be performed in background even after the request timed out, this will help to retrieve result later using queue id or downloaded from Clearout App -> My Activities. Setting 'false' will stop the email discovery immediately when timeout occured Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "name": "Ava Chen"
      },
      "confidenceScore": 1,
      "domain": "string",
      "emails": {
        "business": "ava@example.com",
        "emailAddress": "ava@example.com",
        "role": "ava@example.com"
      },
      "firstName": "Ava",
      "foundOn": "string",
      "fullName": "Ava Chen",
      "lastName": "Chen",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `company.name` | string |  |
| `confidenceScore` | number |  |
| `domain` | string |  |
| `emails` | array<object> |  |
| `emails.business` | string |  |
| `emails.emailAddress` | string |  |
| `emails.role` | string |  |
| `firstName` | string |  |
| `foundOn` | string |  |
| `fullName` | string |  |
| `lastName` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Clearout API, this operation is `POST /email_finder/instant` (base URL `https://api.clearout.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-email-instantly.md) for the provider-specific parameters and requirements.

