# NioLeads: Find Email

Finds a business email in NioLeads by name and domain.

```
GET https://connect.mindcloud.co/v1/universal/nioLeads/latest/actions/find-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NioLeads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nioLeads/latest/actions/find-email?connectionId=$CONNECTION_ID&firstname=Ava&lastname=Chen&domainOrCompany=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "firstname": "Ava",
  "lastname": "Chen",
  "domainOrCompany": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nioLeads/latest/actions/find-email?${params}`, {
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
| `firstname` | string | yes | Person's first name |
| `lastname` | string | yes | Person's last name |
| `domainOrCompany` | string | yes | Email domain or company name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Business email address returned for the requested person when found. |
| `message` | string | Provider message describing the lookup result. |
| `status` | string | Lookup status returned by NioLeads. |

## Native endpoint

Through the native NioLeads API, this operation is `POST /find_email` (base URL `https://v2.nioleads.com/api/openapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-email.md) for the provider-specific parameters and requirements.

