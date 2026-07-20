# Teach 'n Go: Create Prospect

Creates a new prospect in Teach 'n Go.

```
POST https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/create-prospect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teach 'n Go `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/create-prospect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "schoolId": "string",
  "fname": "Ava Chen",
  "lname": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/create-prospect', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "schoolId": "string",
    "fname": "Ava Chen",
    "lname": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schoolId` | string | yes | Your Teach 'n Go school ID. |
| `fname` | string | yes | The prospect's first name. |
| `lname` | string | yes | The prospect's surname. |
| `mobilePhone` | string | no | The prospect's contact number. |
| `emailAddress` | string | no | The prospect's email address. |
| `description` | string | no | Additional information to capture about the prospect. |
| `gender` | string | no | Male, Female, or Not specified. |
| `dateOfBirth` | date | no | The prospect's date of birth. |
| `courseSubject` | string | no | The student's chosen subject. |
| `courseLevel` | string | no | The student's chosen level. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "fname": "Ava Chen",
        "id": "string",
        "lname": "Ava Chen"
      },
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
| `data.fname` | string | Created prospect first name. |
| `data.id` | string | Created Teach 'n Go prospect ID. |
| `data.lname` | string | Created prospect last name. |
| `message` | string | Provider confirmation message. |
| `status` | string | Provider result status. |

## Native endpoint

Through the native Teach 'n Go API, this operation is `POST /LeadsApi/add` (base URL `https://app.teachngo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-prospect.md) for the provider-specific parameters and requirements.

