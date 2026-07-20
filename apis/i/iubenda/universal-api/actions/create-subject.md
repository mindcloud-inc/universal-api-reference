# iubenda: Create Subject

Creates a subject in iubenda.

```
POST https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-subject
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-subject" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-subject', {
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
| `email` | string | no | Subject email address. Example: `alex@example.com`. |
| `firstName` | string | no | Subject first name. Example: `Alex`. |
| `lastName` | string | no | Subject last name. Example: `Morgan`. |
| `verified` | boolean | no | Whether the subject is verified. Example: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fullName` | string | no | Subject full name. Example: `Alex Morgan`. |
| `phones[]` | array<object> | no | Array of phone objects for the subject. |
| `phones[].number` | string | no | A phone number with country code prefix. Example: `+5511999999999`. |
| `phones[].label` | string | no | Label used to identify the phone number. Example: `personal`. |
| `id` | string | no | Subject ID. Auto-filled by iubenda when omitted. Example: `Leave blank to auto-generate`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `timestamp` | string |  |

## Native endpoint

Through the native iubenda API, this operation is `POST /subjects` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subject.md) for the provider-specific parameters and requirements.

