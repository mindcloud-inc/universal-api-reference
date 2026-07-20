# GMass: List Sample Opens

Retrieves sample opens from your GMass account.

```
GET https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-sample-opens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-sample-opens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-sample-opens?${params}`, {
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
      "CampaignID": 1,
      "EmailAddress": "ava@example.com",
      "TimeStamp": "2026-05-07T12:00:00.000Z",
      "UserAgent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CampaignID` | number | GMass campaign ID. |
| `EmailAddress` | string | Email address associated with the event. |
| `TimeStamp` | date | Event timestamp. |
| `UserAgent` | string | User agent of the open event. |

## Native endpoint

Through the native GMass API, this operation is `GET /sample/opens` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sample-opens.md) for the provider-specific parameters and requirements.

