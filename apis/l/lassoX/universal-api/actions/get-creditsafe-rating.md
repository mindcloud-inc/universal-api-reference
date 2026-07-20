# Lasso X: Get CreditSafe Rating

Retrieves a CreditSafe rating from Lasso X by CVR number.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-creditsafe-rating
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-creditsafe-rating?connectionId=$CONNECTION_ID&cvr=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cvr": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-creditsafe-rating?${params}`, {
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
| `cvr` | number | yes | Danish CVR company number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current": {
        "creditCurrency": "string",
        "creditMax": 1,
        "internationalDescription": "string",
        "internationalScore": "string",
        "localDescription": "string",
        "localScore": 1
      },
      "latestChange": "2026-05-07T12:00:00.000Z",
      "pdfUrl": "https://example.com",
      "previous": {
        "creditCurrency": "string",
        "creditMax": 1,
        "internationalScore": "string",
        "localScore": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current.creditCurrency` | string |  |
| `current.creditMax` | number |  |
| `current.internationalDescription` | string |  |
| `current.internationalScore` | string |  |
| `current.localDescription` | string |  |
| `current.localScore` | number |  |
| `latestChange` | date |  |
| `pdfUrl` | string |  |
| `previous.creditCurrency` | string |  |
| `previous.creditMax` | number |  |
| `previous.internationalScore` | string |  |
| `previous.localScore` | number |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /data/creditsafe/rating/:cvr` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-creditsafe-rating.md) for the provider-specific parameters and requirements.

