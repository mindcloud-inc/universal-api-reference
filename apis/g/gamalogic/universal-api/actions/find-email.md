# Gamalogic: Find Email



```
GET https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/find-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gamalogic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/find-email?connectionId=$CONNECTION_ID&firstName=Jessica&lastName=Smith&domain=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "firstName": "Jessica",
  "lastName": "Smith",
  "domain": "example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/find-email?${params}`, {
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
| `firstName` | string | yes | First name of the lead. Example: `Jessica`. |
| `lastName` | string | yes | Last name of the lead. Example: `Smith`. |
| `domain` | string | yes | Company domain or URL to search. Example: `example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `speedRank` | number | no | Optional speed and accuracy setting. Defaults to 0; higher values are slower and more accurate. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "certified": "string",
      "email": "ava@example.com",
      "error": true,
      "errorCode": 1,
      "errorMessage": "string",
      "isCatchall": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certified` | string | Verification state for the discovered email. |
| `email` | string | Verified email address found by Gamalogic. |
| `error` | boolean | Whether the request returned an error. |
| `errorCode` | number | Error code returned when the request fails. |
| `errorMessage` | string | Error message returned when the request fails. |
| `isCatchall` | boolean | Whether the searched domain appears to be catch-all. |

## Native endpoint

Through the native Gamalogic API, this operation is `GET /email-discovery` (base URL `https://gamalogic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-email.md) for the provider-specific parameters and requirements.

