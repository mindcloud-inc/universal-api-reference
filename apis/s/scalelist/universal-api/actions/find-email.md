# Scalelist: Find Email

Finds a contact email in Scalelist.

```
GET https://connect.mindcloud.co/v1/universal/scalelist/latest/actions/find-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scalelist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scalelist/latest/actions/find-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scalelist/latest/actions/find-email?${params}`, {
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
| `fullName` | string | no | Full name of the person to look up. |
| `firstName` | string | no | First name of the person to look up. |
| `lastName` | string | no | Last name of the person to look up. |
| `companyName` | string | no | Company name to help the lookup. |
| `companyWebsite` | string | no | Company website to help the lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "companyDomain": "string",
      "email": "ava@example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Lookup result identifier. |
| `companyDomain` | string | Company domain returned with the lookup result. |
| `email` | string | Email address returned by Scalelist. |
| `status` | string | Email verification status returned by Scalelist. |

## Native endpoint

Through the native Scalelist API, this operation is `GET /api/ext/finder/email` (base URL `https://app.scalelist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-email.md) for the provider-specific parameters and requirements.

