# Shuffll: Set Branding Enabled

Updates branding settings in Shuffll.

```
PUT https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/set-branding-enabled
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/set-branding-enabled" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyValue": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/set-branding-enabled', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyValue": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organization` | object | no | Target organization object when no workspace is provided. Pass an object with an id field. |
| `propertyValue` | boolean | yes | New value for the selected branding property when updating boolean fields like enabled. |
| `workspace` | object | no | Target workspace object. Pass an object with an id field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "about": "string",
      "colors": {},
      "company": {},
      "enabled": true,
      "isDefault": true,
      "logo": "string",
      "logoColors": {},
      "logoW": "string",
      "prompts": [
        {}
      ],
      "pronunciations": [
        {}
      ],
      "videoIdeas": [
        {}
      ],
      "videoIdeaStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `about` | string | About text. |
| `colors` | object | Brand color palette. |
| `company` | object | Brand company details. |
| `enabled` | boolean | Whether branding is enabled. |
| `isDefault` | boolean | Whether branding is default. |
| `logo` | string | Logo asset path. |
| `logoColors` | object | Derived logo color palette. |
| `logoW` | string | Wide logo asset path. |
| `prompts` | array<object> | Prompt suggestions. |
| `pronunciations` | array<object> | Custom pronunciation rules. |
| `videoIdeas` | array<object> | Suggested video ideas. |
| `videoIdeaStatus` | string | Video idea generation status. |

## Native endpoint

Through the native Shuffll API, this operation is `PUT /auth/branding/entity` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-branding-enabled.md) for the provider-specific parameters and requirements.

