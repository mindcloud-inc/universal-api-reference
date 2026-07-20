# iubenda: Update Subject

Updates a subject in iubenda.

```
PUT https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/update-subject
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/update-subject" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subjectId": "bd86b950-af4b-4a4f-9792-1690c18d42f1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/update-subject', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subjectId": "bd86b950-af4b-4a4f-9792-1690c18d42f1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subjectId` | string | yes | Unique identifier of the subject to update Example: `bd86b950-af4b-4a4f-9792-1690c18d42f1`. |
| `email` | string | no | Updated subject email address. Example: `alex@example.com`. |
| `firstName` | string | no | Updated subject first name. Example: `Alex`. |
| `lastName` | string | no | Updated subject last name. Example: `Morgan`. |
| `verified` | boolean | no | Updated subject verified status. Example: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fullName` | string | no | Updated subject full name. Example: `Alex Morgan`. |
| `phones[]` | array<object> | no | Array of phone objects for the subject. |
| `phones[].number` | string | no | A phone number with country code prefix. Example: `+5511999999999`. |
| `phones[].label` | string | no | Label used to identify the phone number. Example: `personal`. |

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

Through the native iubenda API, this operation is `PATCH /subjects/:id` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subject.md) for the provider-specific parameters and requirements.

