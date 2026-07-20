# Crossmint: Get Usage

Retrieves project usage data from Crossmint.

```
GET https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-usage?connectionId=$CONNECTION_ID&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-usage?${params}`, {
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
| `startDate` | string | yes | Enter the month in YYYY-MM format, for example `2026-04`. |
| `endDate` | string | no | Optional end month in YYYY-MM format, for example `2026-04`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "dimension": "string",
          "usage": [
            {
              "activeWallets": 1,
              "month": "string"
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].dimension` | string |  |
| `data[].usage[].activeWallets` | number |  |
| `data[].usage[].month` | string |  |

## Native endpoint

Through the native Crossmint API, this operation is `GET /v1-alpha1/projects/:projectId/usage` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.

