# Routee: Retrieve Verification Statistics for any of your account applications

Retrieves verification statistics for any of your account applications from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-verification-statistics-for-any-of-your-account-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-verification-statistics-for-any-of-your-account-applications?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-verification-statistics-for-any-of-your-account-applications?${params}`, {
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
| `appId` | string | yes | Your application id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationId": "string",
      "perCountry": {
        "GR": {
          "Cancelled": 1,
          "Expired": 1,
          "Failed": 1,
          "Pending": 1,
          "Verified": 1
        }
      },
      "total": "string",
      "totals": {
        "Cancelled": 1,
        "Expired": 1,
        "Failed": 1,
        "Pending": 1,
        "Verified": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationId` | string |  |
| `perCountry` | object |  |
| `perCountry.GR` | object |  |
| `perCountry.GR.Cancelled` | number |  |
| `perCountry.GR.Expired` | number |  |
| `perCountry.GR.Failed` | number |  |
| `perCountry.GR.Pending` | number |  |
| `perCountry.GR.Verified` | number |  |
| `total` | string |  |
| `totals` | object |  |
| `totals.Cancelled` | number |  |
| `totals.Expired` | number |  |
| `totals.Failed` | number |  |
| `totals.Pending` | number |  |
| `totals.Verified` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /2step/reports/applications/:appId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-verification-statistics-for-any-of-your-account-applications.md) for the provider-specific parameters and requirements.

