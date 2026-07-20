# no2bounce: Get Bulk Validation Status

Retrieves bulk validation status from no2bounce by tracking ID.

```
GET https://connect.mindcloud.co/v1/universal/no2bounce/latest/actions/get-bulk-validation-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a no2bounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/no2bounce/latest/actions/get-bulk-validation-status?connectionId=$CONNECTION_ID&trackingId=Paste%20the%20tracking%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingId": "Paste the tracking ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/no2bounce/latest/actions/get-bulk-validation-status?${params}`, {
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
| `trackingId` | string | yes | Use the tracking ID returned by Submit Bulk Validation. Example: `Paste the tracking ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditDebited": 1,
      "overallStatus": "string",
      "percent": 1,
      "result": {
        "downloadFile": "string"
      },
      "totalCredit": 1,
      "totalRecord": 1,
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditDebited` | number |  |
| `overallStatus` | string |  |
| `percent` | number |  |
| `result.downloadFile` | string |  |
| `totalCredit` | number |  |
| `totalRecord` | number |  |
| `trackingId` | string |  |

## Native endpoint

Through the native no2bounce API, this operation is `GET /n2b_validate_bulk` (base URL `https://connect.no2bounce.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-validation-status.md) for the provider-specific parameters and requirements.

