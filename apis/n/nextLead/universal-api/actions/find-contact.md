# NextLead: Find Contact

Finds a contact in NextLead by email or LinkedIn.

```
GET https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/find-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/find-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/find-contact?${params}`, {
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
| `email` | string | no | Contact email address to find. |
| `linkedinUrl` | string | no | LinkedIn URL used when email is not provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "found": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `found` | boolean |  |

## Native endpoint

Through the native NextLead API, this operation is `POST /api/v2/receive/contact/find-contact` (base URL `https://dashboard.nextlead.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-contact.md) for the provider-specific parameters and requirements.

