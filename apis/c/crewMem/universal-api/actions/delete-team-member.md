# CrewMem: Delete Team Member



```
DELETE https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/delete-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrewMem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/delete-team-member?connectionId=$CONNECTION_ID&email=ava%40example.com&teamName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com",
  "teamName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/delete-team-member?${params}`, {
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
| `email` | string | yes | Member email |
| `teamName` | string | yes | Target team name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Provider docs define a generic success payload. |
| `success` | boolean |  |

## Native endpoint

Through the native CrewMem API, this operation is `POST /api/v1/team-member/delete` (base URL `https://crewmem.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-team-member.md) for the provider-specific parameters and requirements.

