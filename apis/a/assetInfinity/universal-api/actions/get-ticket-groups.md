# Asset Infinity: Get Ticket Groups

Retrieves ticket groups from Asset Infinity.

```
GET https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/get-ticket-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asset Infinity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/get-ticket-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/get-ticket-groups?${params}`, {
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
      "data": [
        {
          "dataMode": 1,
          "rowIndexNumber": 1,
          "status": 1,
          "ticketGroupId": 1,
          "ticketGroupName": "Ava Chen",
          "userGroupType": 1
        }
      ],
      "isSuccess": true,
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].dataMode` | number |  |
| `data[].rowIndexNumber` | number |  |
| `data[].status` | number |  |
| `data[].ticketGroupId` | number |  |
| `data[].ticketGroupName` | string |  |
| `data[].userGroupType` | number |  |
| `isSuccess` | boolean |  |
| `message` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native Asset Infinity API, this operation is `POST GetTicketGroupAPI` (base URL `https://api.assetinfinity.io/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-groups.md) for the provider-specific parameters and requirements.

