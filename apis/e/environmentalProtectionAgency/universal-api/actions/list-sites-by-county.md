# Environmental Protection Agency: List Sites By County

Retrieves monitoring sites for a county from EPA AQS.

```
GET https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-sites-by-county
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Environmental Protection Agency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-sites-by-county?connectionId=$CONNECTION_ID&state=37&county=183" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "state": "37",
  "county": "183"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-sites-by-county?${params}`, {
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
| `state` | string | yes | Two-digit state FIPS code, including a leading zero when applicable. Example: `37`. |
| `county` | string | yes | Three-digit county FIPS code within the selected state, including leading zeroes when applicable. Example: `183`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "value_represented": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | EPA AQS code value. |
| `value_represented` | string | Meaning represented by the EPA AQS code. |

## Native endpoint

Through the native Environmental Protection Agency API, this operation is `GET /list/sitesByCounty` (base URL `https://aqs.epa.gov/data/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sites-by-county.md) for the provider-specific parameters and requirements.

