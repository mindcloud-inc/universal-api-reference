# FindyMail: Find People

Finds people in FindyMail.

```
GET https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/find-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FindyMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/find-people?connectionId=$CONNECTION_ID&website=google.com&jobTitles%5B%5D=CEO&count=2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "website": "google.com",
  "jobTitles[]": "CEO",
  "count": "2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/find-people?${params}`, {
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
| `website` | string | yes | Company website to search employees for, for example google.com. Example: `google.com`. |
| `jobTitles[]` | array<string> | yes | Job titles to match, for example CEO. Example: `CEO`. |
| `count` | number | yes | Number of employee results to return. Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "companyWebsite": "string",
      "jobTitle": "string",
      "linkedinUrl": "https://example.com",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string | Employee company name. |
| `companyWebsite` | string | Employee company website. |
| `jobTitle` | string | Employee job title. |
| `linkedinUrl` | string | Employee LinkedIn profile URL. |
| `name` | string | Employee name. |

## Native endpoint

Through the native FindyMail API, this operation is `POST /api/search/employees` (base URL `https://app.findymail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-people.md) for the provider-specific parameters and requirements.

