# ironSource: Get User Ad Revenue Report URL

Retrieves a user ad revenue report URL from ironSource.

```
GET https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-user-ad-revenue-report-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ironSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-user-ad-revenue-report-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-user-ad-revenue-report-url?${params}`, {
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
| `appKey` | string | no | Application key as seen on the LevelPlay platform. |
| `date` | string | no | Report date in YYYY-MM-DD format, UTC timezone. |
| `reportType` | string | no | Report type. The current documented value is 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiration": "2026-05-07T12:00:00.000Z",
      "urls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiration` | date | URL expiration time. |
| `urls` | array<string> | Signed report download URLs. |

## Native endpoint

Through the native ironSource API, this operation is `GET partners/userAdRevenue/v3` (base URL `https://platform.ironsrc.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-ad-revenue-report-url.md) for the provider-specific parameters and requirements.

