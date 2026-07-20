# PeopleDB: Get Contact Info by LinkedIn ID

Retrieves contact info from PeopleDB by LinkedIn ID.

```
GET https://connect.mindcloud.co/v1/universal/peopleDB/latest/actions/get-contact-info-by-linked-in-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PeopleDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDB/latest/actions/get-contact-info-by-linked-in-id?connectionId=$CONNECTION_ID&linkedinId=e.g.%20123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkedinId": "e.g. 123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peopleDB/latest/actions/get-contact-info-by-linked-in-id?${params}`, {
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
| `linkedinId` | number | yes | LinkedIn numeric ID to search by. Example: `e.g. 123456789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailAddresses": [
        "ava@example.com"
      ],
      "facebookUsername": "Ava Chen",
      "githubId": 1,
      "githubLogin": "string",
      "githubUsername": "Ava Chen",
      "linkedinId": 1,
      "linkedinPublicIdentifier": "https://example.com",
      "personalEmailAddresses": [
        "ava@example.com"
      ],
      "phoneNumbers": [
        "string"
      ],
      "twitterUsername": "Ava Chen",
      "workEmailAddresses": [
        "ava@example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAddresses` | array<string> |  |
| `facebookUsername` | string |  |
| `githubId` | number |  |
| `githubLogin` | string |  |
| `githubUsername` | string |  |
| `linkedinId` | number |  |
| `linkedinPublicIdentifier` | string |  |
| `personalEmailAddresses` | array<string> |  |
| `phoneNumbers` | array<string> |  |
| `twitterUsername` | string |  |
| `workEmailAddresses` | array<string> |  |

## Native endpoint

Through the native PeopleDB API, this operation is `GET /people` (base URL `https://peopledb.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-info-by-linked-in-id.md) for the provider-specific parameters and requirements.

