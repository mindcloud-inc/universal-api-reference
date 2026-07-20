# ProvenExpert: Create Profile

Creates a profile in ProvenExpert.

```
POST https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.email": "wizard-provenexpert-profile-1774894073@example.org",
  "data.company": "MindCloud Wizard Child 1774894073"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-profile', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.email": "wizard-provenexpert-profile-1774894073@example.org",
    "data.company": "MindCloud Wizard Child 1774894073"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.email` | string | yes | Email address for the new profile. Example: `wizard-provenexpert-profile-1774894073@example.org`. |
| `data.company` | string | yes | Company name for the new company profile. Example: `MindCloud Wizard Child 1774894073`. |
| `data.description` | string | no | Optional profile description. Example: `Sandbox child profile created by the one-shot batch.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "created": 1,
      "description": "string",
      "email": "ava@example.com",
      "login": {
        "expire": 1,
        "url": "https://example.com"
      },
      "profileUrl": "https://example.com",
      "public": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | Company name for the created profile. |
| `created` | number | Unix timestamp for when the child profile was created. |
| `description` | string | Profile description. |
| `email` | string | Email address for the created profile. |
| `login.expire` | number | Unix timestamp for when the single sign-on URL expires. |
| `login.url` | string | Single sign-on URL returned with the profile. |
| `profileUrl` | string | Public URL for the created profile. |
| `public` | number | Whether the created profile is public. |

## Native endpoint

Through the native ProvenExpert API, this operation is `POST /profile/create` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-profile.md) for the provider-specific parameters and requirements.

