# FindyMail: Find Phone Number

Finds a phone number in FindyMail.

```
GET https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/find-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FindyMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/find-phone-number?connectionId=$CONNECTION_ID&linkedinUrl=https%3A%2F%2Flinkedin.com%2Fin%2Fjohndoe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkedinUrl": "https://linkedin.com/in/johndoe"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/find-phone-number?${params}`, {
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
| `linkedinUrl` | string | yes | LinkedIn profile URL for the person whose direct phone number should be found. Example: `https://linkedin.com/in/johndoe`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "line_type": "string",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `line_type` | string | Phone line type returned by FindyMail. |
| `phone` | string | Direct phone number found for the LinkedIn profile, or null when no phone number is found. |

## Native endpoint

Through the native FindyMail API, this operation is `POST /api/search/phone` (base URL `https://app.findymail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-phone-number.md) for the provider-specific parameters and requirements.

