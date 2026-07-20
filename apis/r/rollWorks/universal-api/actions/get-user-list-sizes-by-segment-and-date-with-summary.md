# RollWorks: Get User List Sizes by Segment and Date with Summary

Retrieves user list sizes in RollWorks by segment and date.

```
GET https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/get-user-list-sizes-by-segment-and-date-with-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RollWorks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/get-user-list-sizes-by-segment-and-date-with-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/get-user-list-sizes-by-segment-and-date-with-summary?${params}`, {
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
      "results": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | object |  |

## Native endpoint

Through the native RollWorks API, this operation is `GET /user-lists/api/v1/userlists/segment` (base URL `https://services.adroll.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-list-sizes-by-segment-and-date-with-summary.md) for the provider-specific parameters and requirements.

