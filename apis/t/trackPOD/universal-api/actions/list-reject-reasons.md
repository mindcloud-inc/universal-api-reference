# Track-POD: List Reject Reasons

Retrieves reject reasons from Track-POD.

```
GET https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/list-reject-reasons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/list-reject-reasons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/list-reject-reasons?${params}`, {
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
      "GoodsIssue": [
        {
          "Id": 1,
          "Name": "Ava Chen"
        }
      ],
      "OrderIssue": [
        {
          "Id": 1,
          "Name": "Ava Chen"
        }
      ],
      "ScanningIssues": [
        {
          "Id": 1,
          "Name": "Ava Chen"
        }
      ],
      "SiteIssue": [
        {
          "Id": 1,
          "Name": "Ava Chen"
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
| `GoodsIssue` | array<object> | List of goods issues |
| `GoodsIssue[].Id` | number | Track-POD unique identifier |
| `GoodsIssue[].Name` | string | Name |
| `OrderIssue` | array<object> | List of order issues |
| `OrderIssue[].Id` | number | Track-POD unique identifier |
| `OrderIssue[].Name` | string | Name |
| `ScanningIssues` | array<object> | List of scanning issues |
| `ScanningIssues[].Id` | number | Track-POD unique identifier |
| `ScanningIssues[].Name` | string | Name |
| `SiteIssue` | array<object> | List of site issues |
| `SiteIssue[].Id` | number | Track-POD unique identifier |
| `SiteIssue[].Name` | string | Name |

## Native endpoint

Through the native Track-POD API, this operation is `GET /RejectReason` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reject-reasons.md) for the provider-specific parameters and requirements.

