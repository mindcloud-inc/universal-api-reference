# Follow Up Boss: Check Duplicate Person

Finds duplicate people in Follow Up Boss by email or phone.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/check-duplicate-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/check-duplicate-person?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/check-duplicate-person?${params}`, {
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
| `email` | string | no | Email address to check for an existing person. |
| `phone` | string | no | Phone number to check for an existing person. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": "string",
      "found": true,
      "matchedBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | string |  |
| `found` | boolean |  |
| `matchedBy` | string |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `GET people/checkDuplicate` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-duplicate-person.md) for the provider-specific parameters and requirements.

