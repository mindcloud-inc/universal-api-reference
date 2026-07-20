# Captain Data: Find People

Finds a person in Captain Data by full name.

```
GET https://connect.mindcloud.co/v1/universal/captainData/latest/actions/find-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Captain Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captainData/latest/actions/find-people?connectionId=$CONNECTION_ID&fullName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fullName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/captainData/latest/actions/find-people?${params}`, {
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
| `fullName` | string | yes | Exact full name to look up. |
| `companyName` | string | no | Optional company name to disambiguate the person search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "li_profile_id": 1,
      "li_profile_url": "https://example.com",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `li_profile_id` | number |  |
| `li_profile_url` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Captain Data API, this operation is `GET /people/find` (base URL `https://api.captaindata.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-people.md) for the provider-specific parameters and requirements.

