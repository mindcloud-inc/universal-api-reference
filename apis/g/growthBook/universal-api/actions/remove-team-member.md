# GrowthBook: Remove members from team

Removes members from a team in GrowthBook.

```
DELETE https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/remove-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/remove-team-member?connectionId=$CONNECTION_ID&id=prj_19g6smo332up7&members=sample" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "prj_19g6smo332up7",
  "members": "sample"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/remove-team-member?${params}`, {
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
| `id` | string | yes | Default: `prj_19g6smo332up7`. |
| `members` | list<string> | yes | Default: `["sample"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |

## Native endpoint

Through the native GrowthBook API, this operation is `DELETE /teams/:id/members` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-team-member.md) for the provider-specific parameters and requirements.

