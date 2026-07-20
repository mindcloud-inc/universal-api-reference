# Routee: Get Statistic Reports for all your account verifications

Retrieves statistic reports for all your account verifications from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-statistic-reports-for-all-your-account-verifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-statistic-reports-for-all-your-account-verifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-statistic-reports-for-all-your-account-verifications?${params}`, {
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
      "perCountry": {
        "GR": {
          "Cancelled": 1,
          "Expired": 1,
          "Failed": 1,
          "Pending": 1,
          "Verified": 1
        }
      },
      "total": 1,
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
| `perCountry` | object |  |
| `perCountry.GR` | object |  |
| `perCountry.GR.Cancelled` | number |  |
| `perCountry.GR.Expired` | number |  |
| `perCountry.GR.Failed` | number |  |
| `perCountry.GR.Pending` | number |  |
| `perCountry.GR.Verified` | number |  |
| `total` | number |  |
| `totals` | object |  |
| `totals.Cancelled` | number |  |
| `totals.Expired` | number |  |
| `totals.Failed` | number |  |
| `totals.Pending` | number |  |
| `totals.Verified` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /2step/reports` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-statistic-reports-for-all-your-account-verifications.md) for the provider-specific parameters and requirements.

