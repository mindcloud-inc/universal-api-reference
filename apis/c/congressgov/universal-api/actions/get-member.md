# Congress.gov: Get Member

Retrieves a member from Congress.gov.

```
GET https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Congress.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-member?connectionId=$CONNECTION_ID&bioguideId=L000174" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bioguideId": "L000174"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-member?${params}`, {
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
      "member": {},
      "request": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `member` | object |  |
| `request` | object |  |

## Native endpoint

Through the native Congress.gov API, this operation is `GET /member/:bioguideId` (base URL `https://api.congress.gov/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member.md) for the provider-specific parameters and requirements.

