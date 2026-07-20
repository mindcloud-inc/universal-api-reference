# Mews: Get All Tax Environments

Retrieves tax environments from Mews.

```
GET https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-tax-environments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-tax-environments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-tax-environments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "countryCode": "string",
      "taxationCodes": [
        "string"
      ],
      "validityEndUtc": "2026-05-07T12:00:00.000Z",
      "validityStartUtc": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Tax-environment code. |
| `countryCode` | string | Country code for the tax environment. |
| `taxationCodes` | array<string> | Taxation codes included in the environment. |
| `validityEndUtc` | date | Validity end timestamp in UTC when present. |
| `validityStartUtc` | date | Validity start timestamp in UTC when present. |

## Native endpoint

Through the native Mews API, this operation is `POST /taxEnvironments/getAll` (base URL `{{credentials.platformAddress}}/api/connector/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-tax-environments.md) for the provider-specific parameters and requirements.

