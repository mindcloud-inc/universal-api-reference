# Missive: Create Response

Creates a response in your Missive workspace.

```
POST https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachments[].base64Data` | string | no | Base64-encoded attachment content |
| `attachments[].filename` | string | no | Attachment filename string |
| `attachments[].id` | string | no | Existing upload ID string |
| `bccFields[].address` | string | no | BCC recipient email address string |
| `bccFields[].name` | string | no | BCC recipient display name string |
| `body` | string | no | HTML string containing the response content |
| `ccFields[].address` | string | no | CC recipient email address string |
| `ccFields[].name` | string | no | CC recipient display name string |
| `externalId` | string | no | External provider ID string |
| `externalSource` | string | no | External provider source string |
| `organization` | string | no | Organization ID string. Either organization or user is required, but not both. |
| `sharedLabels[]` | string | no | Array of organization label ID strings |
| `shareWithTeam` | string | no | Team ID string |
| `subject` | string | no | Response subject string |
| `title` | string | no | Response title string (max 500 characters) |
| `toFields[].address` | string | no | Recipient email address string |
| `toFields[].name` | string | no | Recipient display name string |
| `user` | string | no | User ID string for personal responses. Either organization or user is required, but not both. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responses": [
        {
          "body": "string",
          "externalId": {},
          "externalSource": {},
          "id": "string",
          "modifiedAt": 1,
          "organization": "string",
          "sharedLabels": {},
          "shareWithTeam": {},
          "subject": {},
          "title": {},
          "user": {}
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responses[].body` | string |  |
| `responses[].externalId` | object |  |
| `responses[].externalSource` | object |  |
| `responses[].id` | string |  |
| `responses[].modifiedAt` | number |  |
| `responses[].organization` | string |  |
| `responses[].sharedLabels` | object |  |
| `responses[].shareWithTeam` | object |  |
| `responses[].subject` | object |  |
| `responses[].title` | object |  |
| `responses[].user` | object |  |

## Native endpoint

Through the native Missive API, this operation is `POST /responses` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-response.md) for the provider-specific parameters and requirements.

