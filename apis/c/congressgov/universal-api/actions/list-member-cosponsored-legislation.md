# Congress.gov: List Member Cosponsored Legislation

Retrieves legislation cosponsored by a member in Congress.gov.

```
GET https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-member-cosponsored-legislation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Congress.gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-member-cosponsored-legislation?connectionId=$CONNECTION_ID&limit=25&offset=0&bioguideId=L000174" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "bioguideId": "L000174"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-member-cosponsored-legislation?${params}`, {
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
| `bioguideId` | string | yes | The bioguide identifier for the congressional member. For example, L000174. Example: `L000174`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cosponsoredLegislation": [
        {}
      ],
      "pagination": {},
      "request": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cosponsoredLegislation` | array<object> |  |
| `pagination` | object |  |
| `request` | object |  |

## Native endpoint

Through the native Congress.gov API, this operation is `GET /member/:bioguideId/cosponsored-legislation` (base URL `https://api.congress.gov/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-member-cosponsored-legislation.md) for the provider-specific parameters and requirements.

