# Congress.gov: Get Congress

Retrieves a Congress session from Congress.gov.

```
GET https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-congress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Congress.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-congress?connectionId=$CONNECTION_ID&congress=118" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "congress": "118"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-congress?${params}`, {
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
| `congress` | number | yes | The congress number. For example, 118. Example: `118`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "congress": {},
      "request": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `congress` | object |  |
| `request` | object |  |

## Native endpoint

Through the native Congress.gov API, this operation is `GET /congress/:congress` (base URL `https://api.congress.gov/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-congress.md) for the provider-specific parameters and requirements.

