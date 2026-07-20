# Congress.gov: Get Committee Print

Retrieves a committee print from Congress.gov.

```
GET https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-committee-print
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Congress.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-committee-print?connectionId=$CONNECTION_ID&congress=118&chamber=house&jacketNumber=48144" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "congress": "118",
  "chamber": "house",
  "jacketNumber": "48144"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-committee-print?${params}`, {
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
| `chamber` | string | yes | The chamber name. Values include house, senate, or joint. Example: `house`. |
| `jacketNumber` | number | yes | The jacket number for the print. For example, 48144. Example: `48144`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "committeePrint": {},
      "request": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `committeePrint` | object |  |
| `request` | object |  |

## Native endpoint

Through the native Congress.gov API, this operation is `GET /committee-print/:congress/:chamber/:jacketNumber` (base URL `https://api.congress.gov/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-committee-print.md) for the provider-specific parameters and requirements.

