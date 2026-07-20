# TrainerCentral: Get Learner Info

Retrieves learner info from signup forms in TrainerCentral.

```
GET https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/get-learner-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrainerCentral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/get-learner-info?connectionId=$CONNECTION_ID&email=ava%40example.com&fetchSignupData=true" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com",
  "fetchSignupData": "true"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/get-learner-info?${params}`, {
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
| `email` | string | yes | The learner email address to fetch. |
| `fetchSignupData` | boolean | yes | Set true to include signup form field data with the master fields. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "emailId": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "orgMemberId": "string",
      "status": "string",
      "userFirstName": "Ava",
      "userLastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `emailId` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `orgMemberId` | string |  |
| `status` | string |  |
| `userFirstName` | string |  |
| `userLastName` | string |  |

## Native endpoint

Through the native TrainerCentral API, this operation is `GET /fetchuserdetails.json` (base URL `{{credentials.academyUrl}}/api/v4/{{credentials.orgId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-learner-info.md) for the provider-specific parameters and requirements.

