# Klenty: Create Prospect

Creates a prospect in Klenty.

```
POST https://connect.mindcloud.co/v1/universal/klenty/latest/actions/create-prospect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/create-prospect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/klenty/latest/actions/create-prospect', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account` | string | no | Prospect account field value. |
| `city` | string | no | Prospect city. |
| `companyDomain` | string | no | Prospect company domain. |
| `companyEmail` | string | no | Company email address. |
| `companyPhone` | string | no | Company phone number. |
| `country` | string | no | Prospect country. |
| `department` | string | no | Prospect department. |
| `email` | string | yes | Prospect email address. |
| `linkedinUrl` | string | no | Prospect LinkedIn URL. |
| `location` | string | no | Prospect location. |
| `middleName` | string | no | Prospect middle name. |
| `phone` | string | no | Prospect phone number. |
| `title` | string | no | Prospect job title. |
| `twitterId` | string | no | Prospect Twitter field value. |
| `firstName` | string | no | Prospect first name. |
| `lastName` | string | no | Prospect last name. |
| `company` | string | no | Prospect company name. |
| `list` | string | no | List name to add the prospect to. |
| `tags` | string | no | Pipe-delimited tags to add to the prospect. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fullName` | string | no | Prospect full name. |
| `customFields` | list<object> | no | Custom field key/value entries for the prospect. |
| `owner` | string | no | Owner email address to assign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {
        "email": "ava@example.com",
        "id": "string",
        "prospectOwner": "string",
        "source": "string",
        "status": true
      },
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details.email` | string |  |
| `details.id` | string |  |
| `details.prospectOwner` | string |  |
| `details.source` | string |  |
| `details.status` | boolean |  |
| `status` | boolean |  |

## Native endpoint

Through the native Klenty API, this operation is `POST /prospects` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-prospect.md) for the provider-specific parameters and requirements.

