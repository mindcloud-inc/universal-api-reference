# Scalelist: Find Phone

Finds a contact phone number in Scalelist.

```
GET https://connect.mindcloud.co/v1/universal/scalelist/latest/actions/find-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scalelist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scalelist/latest/actions/find-phone?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scalelist/latest/actions/find-phone?${params}`, {
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
| `linkedinProfileUrl` | string | no | LinkedIn profile URL of the person. |
| `linkedinId` | string | no | LinkedIn ID of the person. |
| `email` | string | no | Email address of the person. |
| `fullName` | string | no | Full name of the person to look up. |
| `firstName` | string | no | First name of the person to look up. |
| `lastName` | string | no | Last name of the person to look up. |
| `companyName` | string | no | Company name to help the lookup. |
| `companyWebsite` | string | no | Company website to help the lookup. |
| `jobTitle` | string | no | Job title of the person. |
| `city` | string | no | City of the person. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "phone": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `phone` | string | Phone number returned by Scalelist. |
| `status` | string | Phone lookup status returned by Scalelist. |

## Native endpoint

Through the native Scalelist API, this operation is `GET /api/ext/finder/phone` (base URL `https://app.scalelist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-phone.md) for the provider-specific parameters and requirements.

