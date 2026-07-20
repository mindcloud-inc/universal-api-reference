# Klenty: Resume Cadence

Resumes cadence for a prospect in Klenty.

```
PUT https://connect.mindcloud.co/v1/universal/klenty/latest/actions/resume-cadence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/resume-cadence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/klenty/latest/actions/resume-cadence', {
  method: 'PUT',
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
| `email` | string | yes | Prospect email to resume cadence for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {
          "errorCode": "string",
          "errorMessage": "string",
          "type": "string"
        }
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors[].errorCode` | string |  |
| `errors[].errorMessage` | string |  |
| `errors[].type` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Klenty API, this operation is `POST /cadences/resume` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resume-cadence.md) for the provider-specific parameters and requirements.

