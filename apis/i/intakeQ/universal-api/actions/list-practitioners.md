# IntakeQ: List Practitioners

Retrieves practitioners from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/list-practitioners
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/list-practitioners?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/list-practitioners?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "completeName": "Ava Chen",
      "dateCreated": "string",
      "email": "ava@example.com",
      "externalPractitionerId": "string",
      "firstName": "Ava",
      "id": "string",
      "isInactive": true,
      "lastName": "Chen",
      "npi": "string",
      "roleName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completeName` | string |  |
| `dateCreated` | string |  |
| `email` | string |  |
| `externalPractitionerId` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `isInactive` | boolean |  |
| `lastName` | string |  |
| `npi` | string |  |
| `roleName` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /practitioners` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-practitioners.md) for the provider-specific parameters and requirements.

